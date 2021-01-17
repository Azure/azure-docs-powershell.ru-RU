---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 488229AF-FD6D-4E1B-B3DA-E57CA781D91E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzRoleAssignment.md
ms.openlocfilehash: 1b96617ce162f3b024cc8a5bd7df2d66c3820c38
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98414140"
---
# <span data-ttu-id="5899a-101">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="5899a-101">Get-AzRoleAssignment</span></span>

## <span data-ttu-id="5899a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5899a-102">SYNOPSIS</span></span>
<span data-ttu-id="5899a-103">Список назначений ролей Azure RBAC в указанной области.</span><span class="sxs-lookup"><span data-stu-id="5899a-103">Lists Azure RBAC role assignments at the specified scope.</span></span>
<span data-ttu-id="5899a-104">По умолчанию здесь перечислены все назначения ролей в выбранной подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="5899a-104">By default it lists all role assignments in the selected Azure subscription.</span></span>
<span data-ttu-id="5899a-105">Используйте соответствующие параметры для списка назначений определенному пользователю или для списка назначений для определенной группы ресурсов или ресурса.</span><span class="sxs-lookup"><span data-stu-id="5899a-105">Use respective parameters to list assignments to a specific user, or to list assignments on a specific resource group or resource.</span></span>

## <span data-ttu-id="5899a-106">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5899a-106">SYNTAX</span></span>

### <span data-ttu-id="5899a-107">EmptyParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5899a-107">EmptyParameterSet (Default)</span></span>
```
Get-AzRoleAssignment [-RoleDefinitionName <String>] [-IncludeClassicAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5899a-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5899a-108">ObjectIdParameterSet</span></span>
```
Get-AzRoleAssignment -ObjectId <String> [-RoleDefinitionName <String>] [-ExpandPrincipalGroups]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5899a-109">ResourceGroupWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5899a-109">ResourceGroupWithObjectIdParameterSet</span></span>
```
Get-AzRoleAssignment -ObjectId <String> -ResourceGroupName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5899a-110">ResourceWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5899a-110">ResourceWithObjectIdParameterSet</span></span>
```
Get-AzRoleAssignment -ObjectId <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5899a-111">ScopeWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5899a-111">ScopeWithObjectIdParameterSet</span></span>
```
Get-AzRoleAssignment -ObjectId <String> [-RoleDefinitionName <String>] -Scope <String>
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5899a-112">RoleIdWithScopeAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5899a-112">RoleIdWithScopeAndObjectIdParameterSet</span></span>
```
Get-AzRoleAssignment [-ObjectId <String>] -RoleDefinitionId <Guid> [-Scope <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5899a-113">ResourceGroupWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="5899a-113">ResourceGroupWithSignInNameParameterSet</span></span>
```
Get-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5899a-114">ResourceWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="5899a-114">ResourceWithSignInNameParameterSet</span></span>
```
Get-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5899a-115">ScopeWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="5899a-115">ScopeWithSignInNameParameterSet</span></span>
```
Get-AzRoleAssignment -SignInName <String> [-RoleDefinitionName <String>] -Scope <String>
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5899a-116">SignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="5899a-116">SignInNameParameterSet</span></span>
```
Get-AzRoleAssignment -SignInName <String> [-RoleDefinitionName <String>] [-ExpandPrincipalGroups]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5899a-117">ResourceGroupWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="5899a-117">ResourceGroupWithSPNParameterSet</span></span>
```
Get-AzRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5899a-118">ResourceWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="5899a-118">ResourceWithSPNParameterSet</span></span>
```
Get-AzRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5899a-119">ScopeWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="5899a-119">ScopeWithSPNParameterSet</span></span>
```
Get-AzRoleAssignment -ServicePrincipalName <String> [-RoleDefinitionName <String>] -Scope <String>
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5899a-120">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="5899a-120">SPNParameterSet</span></span>
```
Get-AzRoleAssignment -ServicePrincipalName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5899a-121">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="5899a-121">ResourceGroupParameterSet</span></span>
```
Get-AzRoleAssignment -ResourceGroupName <String> [-RoleDefinitionName <String>] [-IncludeClassicAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5899a-122">ResourceParameterSet</span><span class="sxs-lookup"><span data-stu-id="5899a-122">ResourceParameterSet</span></span>
```
Get-AzRoleAssignment -ResourceGroupName <String> -ResourceName <String> -ResourceType <String>
 [-ParentResource <String>] [-RoleDefinitionName <String>] [-IncludeClassicAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5899a-123">ScopeParameterSet</span><span class="sxs-lookup"><span data-stu-id="5899a-123">ScopeParameterSet</span></span>
```
Get-AzRoleAssignment [-RoleDefinitionName <String>] -Scope <String> [-IncludeClassicAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5899a-124">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5899a-124">DESCRIPTION</span></span>
<span data-ttu-id="5899a-125">Используйте команду Get-AzRoleAssignment для списка всех назначений ролей, которые эффективны по области действия.</span><span class="sxs-lookup"><span data-stu-id="5899a-125">Use the Get-AzRoleAssignment command to list all role assignments that are effective on a scope.</span></span>
<span data-ttu-id="5899a-126">Без параметров эта команда возвращает все назначения ролей, заданные в подписке.</span><span class="sxs-lookup"><span data-stu-id="5899a-126">Without any parameters, this command returns all the role assignments made under the subscription.</span></span>
<span data-ttu-id="5899a-127">Этот список можно отфильтровать с помощью параметров фильтрации для основных ролей и областей.</span><span class="sxs-lookup"><span data-stu-id="5899a-127">This list can  be filtered using filtering parameters for principal, role and scope.</span></span>
<span data-ttu-id="5899a-128">Необходимо у указывается тема задания.</span><span class="sxs-lookup"><span data-stu-id="5899a-128">The subject of the assignment must be specified.</span></span>
<span data-ttu-id="5899a-129">Чтобы указать пользователя, используйте параметры SignInName или Azure AD ObjectId.</span><span class="sxs-lookup"><span data-stu-id="5899a-129">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="5899a-130">Чтобы указать группу безопасности, используйте параметр Azure AD ObjectId.</span><span class="sxs-lookup"><span data-stu-id="5899a-130">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="5899a-131">Чтобы указать приложение Azure AD, используйте параметры ServicePrincipalName или ObjectId.</span><span class="sxs-lookup"><span data-stu-id="5899a-131">And to specify an Azure AD application, use ServicePrincipalName or ObjectId parameters.</span></span>
<span data-ttu-id="5899a-132">Роль, которая должна быть назначена, должна быть указана с помощью параметра RoleDefinitionName.</span><span class="sxs-lookup"><span data-stu-id="5899a-132">The role that is being assigned must be specified using the RoleDefinitionName parameter.</span></span>
<span data-ttu-id="5899a-133">Может быть указана область, для которой предоставляется доступ.</span><span class="sxs-lookup"><span data-stu-id="5899a-133">The scope at which access is being granted may be specified.</span></span>
<span data-ttu-id="5899a-134">По умолчанию выбранная подписка.</span><span class="sxs-lookup"><span data-stu-id="5899a-134">It defaults to the selected subscription.</span></span> <span data-ttu-id="5899a-135">Область задания можно у определяет с помощью одного из следующих сочетаний параметров a.</span><span class="sxs-lookup"><span data-stu-id="5899a-135">The scope of the assignment can be specified using one of the following parameter combinations a.</span></span>
<span data-ttu-id="5899a-136">Область: это вся полнейская область, начиная с /subscriptions/. \<subscriptionId\></span><span class="sxs-lookup"><span data-stu-id="5899a-136">Scope - This is the fully qualified scope starting with /subscriptions/\<subscriptionId\>.</span></span>
<span data-ttu-id="5899a-137">При этом будут фильтроваться назначения, эффективные в определенной области, то есть все назначения в этой области и выше.</span><span class="sxs-lookup"><span data-stu-id="5899a-137">This will filter assignments that are effective at that particular scope i.e. all assignments at that scope and above.</span></span>
<span data-ttu-id="5899a-138">б)</span><span class="sxs-lookup"><span data-stu-id="5899a-138">b.</span></span>
<span data-ttu-id="5899a-139">ResourceGroupName — имя любой группы ресурсов в рамках подписки.</span><span class="sxs-lookup"><span data-stu-id="5899a-139">ResourceGroupName - Name of any resource group under the subscription.</span></span>
<span data-ttu-id="5899a-140">Это позволит отфильтровать назначения, эффективные в указанной группе ресурсов c.</span><span class="sxs-lookup"><span data-stu-id="5899a-140">This will filter assignments effective at the specified resource group c.</span></span>
<span data-ttu-id="5899a-141">ResourceName, ResourceType, ResourceGroupName и (необязательно) ParentResource — определяет определенный ресурс в подписке и фильтрует назначения, эффективные в этой области.</span><span class="sxs-lookup"><span data-stu-id="5899a-141">ResourceName, ResourceType, ResourceGroupName and (optionally) ParentResource - Identifies a particular resource under the subscription and will filter assignments effective at that resource scope.</span></span>
<span data-ttu-id="5899a-142">Чтобы определить доступ определенного пользователя к подписке, используйте переключатель ExpandPrincipalGroups.</span><span class="sxs-lookup"><span data-stu-id="5899a-142">To determine what access a particular user has in the subscription, use the ExpandPrincipalGroups switch.</span></span>
<span data-ttu-id="5899a-143">В результате будут перечисляться все роли, которые назначены пользователю, а также группам, в которые он входит.</span><span class="sxs-lookup"><span data-stu-id="5899a-143">This will list all roles assigned to the user, and to the groups that the user is member of.</span></span>
<span data-ttu-id="5899a-144">Используйте переключатель IncludeClassicAdministrators, чтобы также отобразить администраторов подписок и соадминистраторов.</span><span class="sxs-lookup"><span data-stu-id="5899a-144">Use the IncludeClassicAdministrators switch to also display the subscription admins and co-admins.</span></span>

## <span data-ttu-id="5899a-145">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5899a-145">EXAMPLES</span></span>

### <span data-ttu-id="5899a-146">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5899a-146">Example 1</span></span>
```
PS C:\> Get-AzRoleAssignment
```

<span data-ttu-id="5899a-147">Перечислить все назначения ролей в подписке</span><span class="sxs-lookup"><span data-stu-id="5899a-147">List all role assignments in the subscription</span></span>

### <span data-ttu-id="5899a-148">Пример 2</span><span class="sxs-lookup"><span data-stu-id="5899a-148">Example 2</span></span>
```
PS C:\> Get-AzRoleAssignment -ResourceGroupName testRG -SignInName john.doe@contoso.com
```

<span data-ttu-id="5899a-149">Получает все назначения ролей, присвоенные пользователю и группам, участником которых он является, в области john.doe@contoso.com testRG или выше.</span><span class="sxs-lookup"><span data-stu-id="5899a-149">Gets all role assignments made to user john.doe@contoso.com, and the groups of which he is member, at the testRG scope or above.</span></span>

### <span data-ttu-id="5899a-150">Пример 3</span><span class="sxs-lookup"><span data-stu-id="5899a-150">Example 3</span></span>
```
PS C:\> Get-AzRoleAssignment -ServicePrincipalName "http://testapp1.com"
```

<span data-ttu-id="5899a-151">Получает все назначения ролей указанного директора-службы</span><span class="sxs-lookup"><span data-stu-id="5899a-151">Gets all role assignments of the specified service principal</span></span>

### <span data-ttu-id="5899a-152">Пример 4</span><span class="sxs-lookup"><span data-stu-id="5899a-152">Example 4</span></span>
```
PS C:\> Get-AzRoleAssignment -Scope "/subscriptions/96231a05-34ce-4eb4-aa6a-70759cbb5e83/resourcegroups/rg1/providers/Microsoft.Web/sites/site1"
```

<span data-ttu-id="5899a-153">Получает назначения ролей в области веб-сайта site1.</span><span class="sxs-lookup"><span data-stu-id="5899a-153">Gets role assignments at the 'site1' website scope.</span></span>

## <span data-ttu-id="5899a-154">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5899a-154">PARAMETERS</span></span>

### <span data-ttu-id="5899a-155">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5899a-155">-DefaultProfile</span></span>
<span data-ttu-id="5899a-156">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="5899a-156">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5899a-157">-ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="5899a-157">-ExpandPrincipalGroups</span></span>
<span data-ttu-id="5899a-158">Если задан этот пункт, возвращает роли, непосредственно назначенные пользователю и группам, участником которых является пользователь (при переходе).</span><span class="sxs-lookup"><span data-stu-id="5899a-158">If specified, returns roles directly assigned to the user and to the groups of which the user is a member (transitively).</span></span>
<span data-ttu-id="5899a-159">Поддерживается только для основного пользователя.</span><span class="sxs-lookup"><span data-stu-id="5899a-159">Supported only for a user principal.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ObjectIdParameterSet, SignInNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5899a-160">-IncludeClassicAdministrators</span><span class="sxs-lookup"><span data-stu-id="5899a-160">-IncludeClassicAdministrators</span></span>
<span data-ttu-id="5899a-161">Здесь также перечислены назначения ролей классическим администраторам подписок (администраторам, администраторам служб и т. д.).</span><span class="sxs-lookup"><span data-stu-id="5899a-161">If specified, also lists subscription classic administrators (co-admins, service admins, etc.) role assignments.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EmptyParameterSet, ObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ScopeWithObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, SignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet, SPNParameterSet, ResourceGroupParameterSet, ResourceParameterSet, ScopeParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5899a-162">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="5899a-162">-ObjectId</span></span>
<span data-ttu-id="5899a-163">ОбъектId Azure AD пользователя, группы или директора службы.</span><span class="sxs-lookup"><span data-stu-id="5899a-163">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>
<span data-ttu-id="5899a-164">Фильтрует все назначения, присвоенные указанному основному.</span><span class="sxs-lookup"><span data-stu-id="5899a-164">Filters all assignments that are made to the specified principal.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ScopeWithObjectIdParameterSet
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: RoleIdWithScopeAndObjectIdParameterSet
Aliases: Id, PrincipalId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5899a-165">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="5899a-165">-ParentResource</span></span>
<span data-ttu-id="5899a-166">Родительский ресурс в иерархии ресурса, указанного с помощью параметра ResourceName.</span><span class="sxs-lookup"><span data-stu-id="5899a-166">The parent resource in the hierarchy of the resource specified using ResourceName parameter.</span></span>
<span data-ttu-id="5899a-167">Используется в сочетании с параметрами ResourceGroupName, ResourceType и ResourceName.</span><span class="sxs-lookup"><span data-stu-id="5899a-167">Must be used in conjunction with ResourceGroupName, ResourceType, and ResourceName parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet, ResourceParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5899a-168">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5899a-168">-ResourceGroupName</span></span>
<span data-ttu-id="5899a-169">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5899a-169">The resource group name.</span></span>
<span data-ttu-id="5899a-170">Содержит список назначений ролей, которые эффективны в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5899a-170">Lists role assignments that are effective at the specified resource group.</span></span>
<span data-ttu-id="5899a-171">При использовании в сочетании с параметрами ResourceName, ResourceType и ParentResource команда перечисляет назначения, эффективные для ресурсов в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5899a-171">When used in conjunction with ResourceName, ResourceType, and ParentResource parameters, the command lists assignments effective at resources within the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ResourceGroupParameterSet, ResourceParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5899a-172">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="5899a-172">-ResourceName</span></span>
<span data-ttu-id="5899a-173">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="5899a-173">The resource name.</span></span>
<span data-ttu-id="5899a-174">Например, storageaccountprod.</span><span class="sxs-lookup"><span data-stu-id="5899a-174">For e.g. storageaccountprod.</span></span>
<span data-ttu-id="5899a-175">Используется в сочетании с параметрами ResourceGroupName, ResourceType и (необязательно)ParentResource.</span><span class="sxs-lookup"><span data-stu-id="5899a-175">Must be used in conjunction with ResourceGroupName, ResourceType, and (optionally)ParentResource parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet, ResourceParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5899a-176">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="5899a-176">-ResourceType</span></span>
<span data-ttu-id="5899a-177">Тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="5899a-177">The resource type.</span></span>
<span data-ttu-id="5899a-178">Например, Microsoft.Network/virtualNetworks.</span><span class="sxs-lookup"><span data-stu-id="5899a-178">For e.g. Microsoft.Network/virtualNetworks.</span></span>
<span data-ttu-id="5899a-179">Используется в сочетании с параметрами ResourceGroupName, ResourceName и (необязательно)ParentResource.</span><span class="sxs-lookup"><span data-stu-id="5899a-179">Must be used in conjunction with ResourceGroupName, ResourceName, and (optionally)ParentResource parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet, ResourceParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5899a-180">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="5899a-180">-RoleDefinitionId</span></span>
<span data-ttu-id="5899a-181">ИД роли, которая назначена основному.</span><span class="sxs-lookup"><span data-stu-id="5899a-181">Id of the Role that is assigned to the principal.</span></span>

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

### <span data-ttu-id="5899a-182">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="5899a-182">-RoleDefinitionName</span></span>
<span data-ttu-id="5899a-183">Роль, которая назначена основному, то есть читатель, участник, администратор виртуальной сети и т. д.</span><span class="sxs-lookup"><span data-stu-id="5899a-183">Role that is assigned to the principal i.e. Reader, Contributor, Virtual Network Administrator, etc.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ScopeWithObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, SignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet, SPNParameterSet, ResourceGroupParameterSet, ResourceParameterSet, ScopeParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5899a-184">-Scope</span><span class="sxs-lookup"><span data-stu-id="5899a-184">-Scope</span></span>
<span data-ttu-id="5899a-185">Область назначения роли.</span><span class="sxs-lookup"><span data-stu-id="5899a-185">The Scope of the role assignment.</span></span>
<span data-ttu-id="5899a-186">В формате относительного URI.</span><span class="sxs-lookup"><span data-stu-id="5899a-186">In the format of relative URI.</span></span>
<span data-ttu-id="5899a-187">Например, /subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG.</span><span class="sxs-lookup"><span data-stu-id="5899a-187">For e.g. /subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG.</span></span>
<span data-ttu-id="5899a-188">Оно должно начинаться с "/subscriptions/{id}".</span><span class="sxs-lookup"><span data-stu-id="5899a-188">It must start with "/subscriptions/{id}".</span></span>
<span data-ttu-id="5899a-189">Эта команда фильтрует все назначения, которые эффективны в этой области.</span><span class="sxs-lookup"><span data-stu-id="5899a-189">The command filters all assignments that are effective at that scope.</span></span>

```yaml
Type: System.String
Parameter Sets: ScopeWithObjectIdParameterSet, ScopeWithSignInNameParameterSet, ScopeWithSPNParameterSet, ScopeParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: RoleIdWithScopeAndObjectIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5899a-190">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="5899a-190">-ServicePrincipalName</span></span>
<span data-ttu-id="5899a-191">ServicePrincipalName основной услуги.</span><span class="sxs-lookup"><span data-stu-id="5899a-191">The ServicePrincipalName of the service principal.</span></span>
<span data-ttu-id="5899a-192">Фильтрует все назначения, присвоенные указанному приложению Azure AD.</span><span class="sxs-lookup"><span data-stu-id="5899a-192">Filters all assignments that are made to the specified Azure AD application.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet, SPNParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5899a-193">-SignInName</span><span class="sxs-lookup"><span data-stu-id="5899a-193">-SignInName</span></span>
<span data-ttu-id="5899a-194">Адрес электронной почты или имя директора пользователя.</span><span class="sxs-lookup"><span data-stu-id="5899a-194">The email address or the user principal name of the user.</span></span>
<span data-ttu-id="5899a-195">Фильтрует все назначения, присвоенные указанному пользователю.</span><span class="sxs-lookup"><span data-stu-id="5899a-195">Filters all assignments that are made to the specified user.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, SignInNameParameterSet
Aliases: Email, UserPrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5899a-196">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5899a-196">CommonParameters</span></span>
<span data-ttu-id="5899a-197">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5899a-197">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5899a-198">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5899a-198">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5899a-199">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5899a-199">INPUTS</span></span>

### <span data-ttu-id="5899a-200">System.String</span><span class="sxs-lookup"><span data-stu-id="5899a-200">System.String</span></span>

### <span data-ttu-id="5899a-201">System.Guid</span><span class="sxs-lookup"><span data-stu-id="5899a-201">System.Guid</span></span>

## <span data-ttu-id="5899a-202">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5899a-202">OUTPUTS</span></span>

### <span data-ttu-id="5899a-203">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="5899a-203">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>

## <span data-ttu-id="5899a-204">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5899a-204">NOTES</span></span>
<span data-ttu-id="5899a-205">Ключевые слова: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span><span class="sxs-lookup"><span data-stu-id="5899a-205">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="5899a-206">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5899a-206">RELATED LINKS</span></span>

[<span data-ttu-id="5899a-207">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="5899a-207">New-AzRoleAssignment</span></span>](./New-AzRoleAssignment.md)

[<span data-ttu-id="5899a-208">Remove-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="5899a-208">Remove-AzRoleAssignment</span></span>](./Remove-AzRoleAssignment.md)

[<span data-ttu-id="5899a-209">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="5899a-209">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)

