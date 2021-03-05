---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 8C1D738C-825D-4718-AD2A-9CFEAA7DBD3B
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-azroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzRoleAssignment.md
ms.openlocfilehash: d941e5cc3bf4a3f2363aa8369a7f5b0518ba2e07
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005800"
---
# <span data-ttu-id="807ae-101">Remove-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="807ae-101">Remove-AzRoleAssignment</span></span>

## <span data-ttu-id="807ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="807ae-102">SYNOPSIS</span></span>
<span data-ttu-id="807ae-103">Удаляет назначение роли для указанного директора, которому назначена определенная роль в определенной области.</span><span class="sxs-lookup"><span data-stu-id="807ae-103">Removes a role assignment to the specified principal who is assigned to a particular role at a particular scope.</span></span>

## <span data-ttu-id="807ae-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="807ae-104">SYNTAX</span></span>

### <span data-ttu-id="807ae-105">EmptyParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="807ae-105">EmptyParameterSet (Default)</span></span>
```
Remove-AzRoleAssignment -ObjectId <String> [-Scope <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="807ae-106">ResourceWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="807ae-106">ResourceWithObjectIdParameterSet</span></span>
```
Remove-AzRoleAssignment -ObjectId <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="807ae-107">ResourceGroupWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="807ae-107">ResourceGroupWithObjectIdParameterSet</span></span>
```
Remove-AzRoleAssignment -ObjectId <String> -ResourceGroupName <String> -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="807ae-108">ScopeWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="807ae-108">ScopeWithObjectIdParameterSet</span></span>
```
Remove-AzRoleAssignment -ObjectId <String> [-Scope <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="807ae-109">RoleIdWithScopeAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="807ae-109">RoleIdWithScopeAndObjectIdParameterSet</span></span>
```
Remove-AzRoleAssignment -ObjectId <String> [-Scope <String>] -RoleDefinitionId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="807ae-110">ResourceWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="807ae-110">ResourceWithSignInNameParameterSet</span></span>
```
Remove-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="807ae-111">ResourceGroupWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="807ae-111">ResourceGroupWithSignInNameParameterSet</span></span>
```
Remove-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="807ae-112">ScopeWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="807ae-112">ScopeWithSignInNameParameterSet</span></span>
```
Remove-AzRoleAssignment -SignInName <String> [-Scope <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="807ae-113">ResourceWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="807ae-113">ResourceWithSPNParameterSet</span></span>
```
Remove-AzRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="807ae-114">ResourceGroupWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="807ae-114">ResourceGroupWithSPNParameterSet</span></span>
```
Remove-AzRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="807ae-115">ScopeWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="807ae-115">ScopeWithSPNParameterSet</span></span>
```
Remove-AzRoleAssignment -ServicePrincipalName <String> [-Scope <String>] -RoleDefinitionName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="807ae-116">RoleAssignmentParameterSet</span><span class="sxs-lookup"><span data-stu-id="807ae-116">RoleAssignmentParameterSet</span></span>
```
Remove-AzRoleAssignment [-PassThru] [-InputObject] <PSRoleAssignment>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="807ae-117">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="807ae-117">DESCRIPTION</span></span>
<span data-ttu-id="807ae-118">С помощью Remove-AzRoleAssignment управления можно ото всех основных ролей в заданной области и роли.</span><span class="sxs-lookup"><span data-stu-id="807ae-118">Use the Remove-AzRoleAssignment commandlet to revoke access to any principal at given scope and given role.</span></span>
<span data-ttu-id="807ae-119">Объект назначения, то есть основной должен быть указан.</span><span class="sxs-lookup"><span data-stu-id="807ae-119">The object of the assignment i.e. the principal MUST be specified.</span></span>
<span data-ttu-id="807ae-120">Основным может быть пользователь (с помощью параметров SignInName или ObjectId для идентификации пользователя), группа безопасности (с помощью параметра ObjectId для идентификации группы) или главная служба (для определения параметра ServicePrincipalName или ObjectId используется параметр ServicePrincipal).</span><span class="sxs-lookup"><span data-stu-id="807ae-120">The principal can be a user (use SignInName or ObjectId parameters to identify a user), security group (use ObjectId parameter to identify a group) or service principal (use ServicePrincipalName or ObjectId parameters to identify a ServicePrincipal.</span></span>
<span data-ttu-id="807ae-121">Роль, которая назначена основной, должна быть указана с помощью параметра RoleDefinitionName.</span><span class="sxs-lookup"><span data-stu-id="807ae-121">The role that the principal is assigned to MUST be specified using the RoleDefinitionName parameter.</span></span>
<span data-ttu-id="807ae-122">Область назначения может быть указана и, если не указана, по умолчанию задана область действия подписки, т. е. оно попытается удалить назначение указанному основному заданию и роли в области подписки.</span><span class="sxs-lookup"><span data-stu-id="807ae-122">The scope of the assignment MAY be specified and if not specified, defaults to the subscription scope i.e. it will try to delete an assignment to the specified principal and role at the subscription scope.</span></span>
<span data-ttu-id="807ae-123">Область назначения можно укакручить с помощью одного из следующих параметров:</span><span class="sxs-lookup"><span data-stu-id="807ae-123">The scope of the assignment can be specified using one of the following parameters.</span></span>
<span data-ttu-id="807ae-124">а)</span><span class="sxs-lookup"><span data-stu-id="807ae-124">a.</span></span>
<span data-ttu-id="807ae-125">Область: это вся полнейская область, начиная с \<subscriptionId\> /subscriptions/b.</span><span class="sxs-lookup"><span data-stu-id="807ae-125">Scope - This is the fully qualified scope starting with /subscriptions/\<subscriptionId\> b.</span></span>
<span data-ttu-id="807ae-126">ResourceGroupName — имя любой группы ресурсов в рамках подписки.</span><span class="sxs-lookup"><span data-stu-id="807ae-126">ResourceGroupName - Name of any resource group under the subscription.</span></span>
<span data-ttu-id="807ae-127">в.</span><span class="sxs-lookup"><span data-stu-id="807ae-127">c.</span></span>
<span data-ttu-id="807ae-128">ResourceName, ResourceType, ResourceGroupName и (необязательно) ParentResource — определяет определенный ресурс в подписке.</span><span class="sxs-lookup"><span data-stu-id="807ae-128">ResourceName, ResourceType, ResourceGroupName and (optionally) ParentResource - Identifies a particular resource under the subscription.</span></span>

## <span data-ttu-id="807ae-129">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="807ae-129">EXAMPLES</span></span>

### <span data-ttu-id="807ae-130">Пример 1</span><span class="sxs-lookup"><span data-stu-id="807ae-130">Example 1</span></span>
```
PS C:\> Remove-AzRoleAssignment -ResourceGroupName rg1 -SignInName john.doe@contoso.com -RoleDefinitionName Reader
```

<span data-ttu-id="807ae-131">Удаляет назначение ролей для тех, кому назначена роль "Читатель" в области "Группа ресурсов john.doe@contoso.com rg1".</span><span class="sxs-lookup"><span data-stu-id="807ae-131">Removes a role assignment for john.doe@contoso.com who is assigned to the Reader role at the rg1 resourcegroup scope.</span></span>

### <span data-ttu-id="807ae-132">Пример 2</span><span class="sxs-lookup"><span data-stu-id="807ae-132">Example 2</span></span>
```
PS C:\> Remove-AzRoleAssignment -ObjectId 36f81fc3-b00f-48cd-8218-3879f51ff39f -RoleDefinitionName Reader
```

<span data-ttu-id="807ae-133">Удаляет назначение роли для группы, которая была определена объективным объектом и назначена роли "Читатель".</span><span class="sxs-lookup"><span data-stu-id="807ae-133">Removes the role assignment to the group principal identified by the ObjectId and assigned to the Reader role.</span></span>
<span data-ttu-id="807ae-134">По умолчанию для удаления задания используется текущая подписка.</span><span class="sxs-lookup"><span data-stu-id="807ae-134">Defaults to using the current subscription as the scope to find the assignment to be deleted.</span></span>

### <span data-ttu-id="807ae-135">Пример 3</span><span class="sxs-lookup"><span data-stu-id="807ae-135">Example 3</span></span>
```
PS C:\> $roleassignment = Get-AzRoleAssignment |Select-Object -First 1 -Wait
PS C:\> Remove-AzRoleAssignment -InputObject $roleassignment
```

<span data-ttu-id="807ae-136">Удаляет первый объект назначения роли, извлеченный Get-AzRoleAssignment командлета.</span><span class="sxs-lookup"><span data-stu-id="807ae-136">Removes the first role assignment object which is fetched from the Get-AzRoleAssignment commandlet.</span></span>

## <span data-ttu-id="807ae-137">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="807ae-137">PARAMETERS</span></span>

### <span data-ttu-id="807ae-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="807ae-138">-DefaultProfile</span></span>
<span data-ttu-id="807ae-139">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="807ae-139">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="807ae-140">-InputObject</span><span class="sxs-lookup"><span data-stu-id="807ae-140">-InputObject</span></span>
<span data-ttu-id="807ae-141">Объект "Назначение ролей".</span><span class="sxs-lookup"><span data-stu-id="807ae-141">Role Assignment object.</span></span>

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

### <span data-ttu-id="807ae-142">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="807ae-142">-ObjectId</span></span>
<span data-ttu-id="807ae-143">ОбъектId Azure AD пользователя, группы или основной службы.</span><span class="sxs-lookup"><span data-stu-id="807ae-143">Azure AD ObjectId of the user, group or service principal.</span></span>

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

### <span data-ttu-id="807ae-144">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="807ae-144">-ParentResource</span></span>
<span data-ttu-id="807ae-145">Родительский ресурс в иерархии (из ресурса, указанного с помощью параметра ResourceName), если он имеется.</span><span class="sxs-lookup"><span data-stu-id="807ae-145">The parent resource in the hierarchy(of the resource specified using ResourceName parameter), if any.</span></span>
<span data-ttu-id="807ae-146">Необходимо использовать в сочетании с параметрами ResourceGroupName, ResourceType и ResourceName для создания иерархической области в виде относительного URI, определяемого ресурсом.</span><span class="sxs-lookup"><span data-stu-id="807ae-146">Must be used in conjunction with ResourceGroupName, ResourceType and ResourceName parameters to construct a hierarchical scope in the form of a relative URI that identifies the resource.</span></span>

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

### <span data-ttu-id="807ae-147">-PassThru</span><span class="sxs-lookup"><span data-stu-id="807ae-147">-PassThru</span></span>
<span data-ttu-id="807ae-148">Отображение удаленного назначения роли, если он задан.</span><span class="sxs-lookup"><span data-stu-id="807ae-148">If specified, displays the deleted role assignment</span></span>

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

### <span data-ttu-id="807ae-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="807ae-149">-ResourceGroupName</span></span>
<span data-ttu-id="807ae-150">Имя группы ресурсов, назначенной роли.</span><span class="sxs-lookup"><span data-stu-id="807ae-150">The resource group name that the role is assigned to.</span></span>
<span data-ttu-id="807ae-151">Пытается удалить назначение в указанной области действия группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="807ae-151">Attempts to delete an assignment at the specified resource group scope.</span></span>
<span data-ttu-id="807ae-152">При использовании в сочетании с параметрами ResourceName, ResourceType и (необязательно)ParentResource команда формирует иерархическую область в виде относительного URI, определяемого ресурсом.</span><span class="sxs-lookup"><span data-stu-id="807ae-152">When used in conjunction with ResourceName, ResourceType and (optionally)ParentResource parameters, the command constructs a hierarchical scope in the form of a relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="807ae-153">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="807ae-153">-ResourceName</span></span>
<span data-ttu-id="807ae-154">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="807ae-154">The resource name.</span></span>
<span data-ttu-id="807ae-155">Например, storageaccountprod.</span><span class="sxs-lookup"><span data-stu-id="807ae-155">For e.g. storageaccountprod.</span></span>
<span data-ttu-id="807ae-156">Необходимо использовать в сочетании с параметрами ResourceGroupName, ResourceType и (необязательно)ParentResource, чтобы построить иерархическую область в виде относительного URI, определяемого ресурсом, и удаления назначения в этой области.</span><span class="sxs-lookup"><span data-stu-id="807ae-156">Must be used in conjunction with ResourceGroupName, ResourceType and (optionally)ParentResource parameters, to construct a hierarchical scope in the form of a relative URI that identifies the resource and delete an assignment at that scope.</span></span>

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

### <span data-ttu-id="807ae-157">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="807ae-157">-ResourceType</span></span>
<span data-ttu-id="807ae-158">Тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="807ae-158">The resource type.</span></span>
<span data-ttu-id="807ae-159">Например, Microsoft.Network/virtualNetworks.</span><span class="sxs-lookup"><span data-stu-id="807ae-159">For e.g. Microsoft.Network/virtualNetworks.</span></span>
<span data-ttu-id="807ae-160">Необходимо использовать в сочетании с параметрами ResourceGroupName, ResourceName и (необязательно)ParentResource для создания иерархической области в виде относительного URI, определяемого ресурсом, и удаления назначения из этой области.</span><span class="sxs-lookup"><span data-stu-id="807ae-160">Must be used in conjunction with ResourceGroupName, ResourceName and (optionally)ParentResource parameters to construct a hierarchical scope in the form of a relative URI that identifies the resource and delete an assignment at that resource scope.</span></span>

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

### <span data-ttu-id="807ae-161">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="807ae-161">-RoleDefinitionId</span></span>
<span data-ttu-id="807ae-162">ИД роли "СДБ", для которой нужно удалить назначение.</span><span class="sxs-lookup"><span data-stu-id="807ae-162">Id of the RBAC role for which the assignment needs to be deleted.</span></span>

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

### <span data-ttu-id="807ae-163">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="807ae-163">-RoleDefinitionName</span></span>
<span data-ttu-id="807ae-164">Имя роли СДВ, для которой нужно удалить назначение, например "Читатель", "Участник", "Виртуальный администратор сети" и т. д.</span><span class="sxs-lookup"><span data-stu-id="807ae-164">Name of the RBAC role for which the assignment needs to be deleted i.e. Reader, Contributor, Virtual Network Administrator, etc.</span></span>

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

### <span data-ttu-id="807ae-165">-Scope</span><span class="sxs-lookup"><span data-stu-id="807ae-165">-Scope</span></span>
<span data-ttu-id="807ae-166">Область удаления назначения роли.</span><span class="sxs-lookup"><span data-stu-id="807ae-166">The Scope of the role assignment to be deleted.</span></span>
<span data-ttu-id="807ae-167">В формате относительного URI.</span><span class="sxs-lookup"><span data-stu-id="807ae-167">In the format of relative URI.</span></span>
<span data-ttu-id="807ae-168">Например: "/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG".</span><span class="sxs-lookup"><span data-stu-id="807ae-168">For e.g. "/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG".</span></span>
<span data-ttu-id="807ae-169">Если он не указан, будет предпринята попытка удалить роль на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="807ae-169">If not specified, will attempt to delete the role at subscription level.</span></span>
<span data-ttu-id="807ae-170">Если указано, оно должно начинаться с "/subscriptions/{id}".</span><span class="sxs-lookup"><span data-stu-id="807ae-170">If specified, it should start with "/subscriptions/{id}".</span></span>

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

### <span data-ttu-id="807ae-171">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="807ae-171">-ServicePrincipalName</span></span>
<span data-ttu-id="807ae-172">Имя ServicePrincipalName приложения Azure AD</span><span class="sxs-lookup"><span data-stu-id="807ae-172">The ServicePrincipalName of the Azure AD application</span></span>

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

### <span data-ttu-id="807ae-173">-SignInName</span><span class="sxs-lookup"><span data-stu-id="807ae-173">-SignInName</span></span>
<span data-ttu-id="807ae-174">Адрес электронной почты или имя директора пользователя.</span><span class="sxs-lookup"><span data-stu-id="807ae-174">The email address or the user principal name of the user.</span></span>

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

### <span data-ttu-id="807ae-175">-Confirm</span><span class="sxs-lookup"><span data-stu-id="807ae-175">-Confirm</span></span>
<span data-ttu-id="807ae-176">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="807ae-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="807ae-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="807ae-177">-WhatIf</span></span>
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

### <span data-ttu-id="807ae-178">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="807ae-178">CommonParameters</span></span>
<span data-ttu-id="807ae-179">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="807ae-179">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="807ae-180">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="807ae-180">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="807ae-181">INPUTS</span><span class="sxs-lookup"><span data-stu-id="807ae-181">INPUTS</span></span>

### <span data-ttu-id="807ae-182">System.String</span><span class="sxs-lookup"><span data-stu-id="807ae-182">System.String</span></span>

### <span data-ttu-id="807ae-183">System.Guid</span><span class="sxs-lookup"><span data-stu-id="807ae-183">System.Guid</span></span>

### <span data-ttu-id="807ae-184">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="807ae-184">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>

## <span data-ttu-id="807ae-185">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="807ae-185">OUTPUTS</span></span>

### <span data-ttu-id="807ae-186">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="807ae-186">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>

## <span data-ttu-id="807ae-187">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="807ae-187">NOTES</span></span>
<span data-ttu-id="807ae-188">Ключевые слова: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span><span class="sxs-lookup"><span data-stu-id="807ae-188">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="807ae-189">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="807ae-189">RELATED LINKS</span></span>

[<span data-ttu-id="807ae-190">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="807ae-190">New-AzRoleAssignment</span></span>](./New-AzRoleAssignment.md)

[<span data-ttu-id="807ae-191">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="807ae-191">Get-AzRoleAssignment</span></span>](./Get-AzRoleAssignment.md)

[<span data-ttu-id="807ae-192">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="807ae-192">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)

