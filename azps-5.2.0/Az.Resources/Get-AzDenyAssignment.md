---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdenyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDenyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDenyAssignment.md
ms.openlocfilehash: 22acfc03afa4758c44d6c6f02ac1d734c90a806b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98325391"
---
# <span data-ttu-id="b4800-101">Get-AzDenyAssignment</span><span class="sxs-lookup"><span data-stu-id="b4800-101">Get-AzDenyAssignment</span></span>

## <span data-ttu-id="b4800-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4800-102">SYNOPSIS</span></span>
<span data-ttu-id="b4800-103">Список заданий запрета Azure RBAC в указанной области.</span><span class="sxs-lookup"><span data-stu-id="b4800-103">Lists Azure RBAC deny assignments at the specified scope.</span></span>
<span data-ttu-id="b4800-104">По умолчанию в нем перечислены все отступные назначения в выбранной подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="b4800-104">By default it lists all deny assignments in the selected Azure subscription.</span></span>
<span data-ttu-id="b4800-105">С помощью соответствующих параметров можно запретить назначение определенному пользователю или запретить назначение определенной группе ресурсов или ресурсу.</span><span class="sxs-lookup"><span data-stu-id="b4800-105">Use respective parameters to list deny assignments to a specific user, or to list deny assignments on a specific resource group or resource.</span></span>

## <span data-ttu-id="b4800-106">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b4800-106">SYNTAX</span></span>

### <span data-ttu-id="b4800-107">EmptyParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b4800-107">EmptyParameterSet (Default)</span></span>
```
Get-AzDenyAssignment [-Scope <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4800-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4800-108">ObjectIdParameterSet</span></span>
```
Get-AzDenyAssignment -ObjectId <Guid> [-ExpandPrincipalGroups] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b4800-109">ResourceGroupWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4800-109">ResourceGroupWithObjectIdParameterSet</span></span>
```
Get-AzDenyAssignment -ObjectId <Guid> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b4800-110">ResourceWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4800-110">ResourceWithObjectIdParameterSet</span></span>
```
Get-AzDenyAssignment -ObjectId <Guid> -ResourceGroupName <String> -ResourceName <String> -ResourceType <String>
 [-ParentResource <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4800-111">ScopeWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4800-111">ScopeWithObjectIdParameterSet</span></span>
```
Get-AzDenyAssignment -ObjectId <Guid> -Scope <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b4800-112">ResourceGroupWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4800-112">ResourceGroupWithSignInNameParameterSet</span></span>
```
Get-AzDenyAssignment -SignInName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4800-113">ResourceWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4800-113">ResourceWithSignInNameParameterSet</span></span>
```
Get-AzDenyAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b4800-114">ScopeWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4800-114">ScopeWithSignInNameParameterSet</span></span>
```
Get-AzDenyAssignment -SignInName <String> -Scope <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b4800-115">SignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4800-115">SignInNameParameterSet</span></span>
```
Get-AzDenyAssignment -SignInName <String> [-ExpandPrincipalGroups] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b4800-116">ResourceGroupWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4800-116">ResourceGroupWithSPNParameterSet</span></span>
```
Get-AzDenyAssignment -ServicePrincipalName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4800-117">ResourceWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4800-117">ResourceWithSPNParameterSet</span></span>
```
Get-AzDenyAssignment -ServicePrincipalName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b4800-118">ScopeWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4800-118">ScopeWithSPNParameterSet</span></span>
```
Get-AzDenyAssignment -ServicePrincipalName <String> -Scope <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b4800-119">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4800-119">SPNParameterSet</span></span>
```
Get-AzDenyAssignment -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b4800-120">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4800-120">ResourceGroupParameterSet</span></span>
```
Get-AzDenyAssignment -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b4800-121">ResourceParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4800-121">ResourceParameterSet</span></span>
```
Get-AzDenyAssignment -ResourceGroupName <String> -ResourceName <String> -ResourceType <String>
 [-ParentResource <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4800-122">ScopeParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4800-122">ScopeParameterSet</span></span>
```
Get-AzDenyAssignment -Scope <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4800-123">DenyAssignmentIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4800-123">DenyAssignmentIdParameterSet</span></span>
```
Get-AzDenyAssignment [-Scope <String>] -Id <Guid> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b4800-124">DenyAssignmentNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4800-124">DenyAssignmentNameParameterSet</span></span>
```
Get-AzDenyAssignment [-Scope <String>] -DenyAssignmentName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b4800-125">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b4800-125">DESCRIPTION</span></span>
<span data-ttu-id="b4800-126">Используйте команду Get-AzDenyAssignment для списка всех запрещенных назначений, которые эффективны в рамках области.</span><span class="sxs-lookup"><span data-stu-id="b4800-126">Use the Get-AzDenyAssignment command to list all deny assignments that are effective on a scope.</span></span>
<span data-ttu-id="b4800-127">Если не у вас нет параметров, эта команда возвращает все запреты, сделанные в рамках подписки.</span><span class="sxs-lookup"><span data-stu-id="b4800-127">Without any parameters, this command returns all the deny assignments made under the subscription.</span></span>
<span data-ttu-id="b4800-128">Этот список можно отфильтровать с помощью параметров фильтрации для основного задания, запрета имени назначения и области.</span><span class="sxs-lookup"><span data-stu-id="b4800-128">This list can  be filtered using filtering parameters for principal, deny assignment name and scope.</span></span>
<span data-ttu-id="b4800-129">Чтобы указать пользователя, используйте параметры SignInName или Azure AD ObjectId.</span><span class="sxs-lookup"><span data-stu-id="b4800-129">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="b4800-130">Чтобы указать группу безопасности, используйте параметр Azure AD ObjectId.</span><span class="sxs-lookup"><span data-stu-id="b4800-130">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="b4800-131">Чтобы указать приложение Azure AD, используйте параметры ServicePrincipalName или ObjectId.</span><span class="sxs-lookup"><span data-stu-id="b4800-131">And to specify an Azure AD application, use ServicePrincipalName or ObjectId parameters.</span></span>
<span data-ttu-id="b4800-132">Может быть указана область, в которой отказано в доступе.</span><span class="sxs-lookup"><span data-stu-id="b4800-132">The scope at which access is being denied may be specified.</span></span>
<span data-ttu-id="b4800-133">По умолчанию выбранная подписка.</span><span class="sxs-lookup"><span data-stu-id="b4800-133">It defaults to the selected subscription.</span></span>
<span data-ttu-id="b4800-134">Область запрета задания можно укакнуть, используя одно из следующих сочетаний параметров a.</span><span class="sxs-lookup"><span data-stu-id="b4800-134">The scope of the deny assignment can be specified using one of the following parameter combinations a.</span></span>
<span data-ttu-id="b4800-135">Область: это вся полнейская область, начиная с /subscriptions/. \<subscriptionId\></span><span class="sxs-lookup"><span data-stu-id="b4800-135">Scope - This is the fully qualified scope starting with /subscriptions/\<subscriptionId\>.</span></span>
<span data-ttu-id="b4800-136">При этом будут фильтроваться запреты назначений, которые эффективны в определенной области, то есть все запретить назначения в этой области и выше.</span><span class="sxs-lookup"><span data-stu-id="b4800-136">This will filter deny assignments that are effective at that particular scope i.e. all deny assignments at that scope and above.</span></span>
<span data-ttu-id="b4800-137">б)</span><span class="sxs-lookup"><span data-stu-id="b4800-137">b.</span></span>
<span data-ttu-id="b4800-138">ResourceGroupName — имя любой группы ресурсов в рамках подписки.</span><span class="sxs-lookup"><span data-stu-id="b4800-138">ResourceGroupName - Name of any resource group under the subscription.</span></span>
<span data-ttu-id="b4800-139">При этом будут фильтроваться назначения, эффективные для указанной группы ресурсов, то есть все отфильтровать назначения в этой области и выше.</span><span class="sxs-lookup"><span data-stu-id="b4800-139">This will filter assignments effective at the specified resource group i.e. all deny assignments at that scope and above.</span></span>
<span data-ttu-id="b4800-140">в.</span><span class="sxs-lookup"><span data-stu-id="b4800-140">c.</span></span>
<span data-ttu-id="b4800-141">ResourceName, ResourceType, ResourceGroupName и (необязательно) ParentResource — определяет определенный ресурс в подписке и фильтрует запреты назначений, эффективные в этой области.</span><span class="sxs-lookup"><span data-stu-id="b4800-141">ResourceName, ResourceType, ResourceGroupName and (optionally) ParentResource - Identifies a particular resource under the subscription and will filter deny assignments effective at that resource scope.</span></span>
<span data-ttu-id="b4800-142">Чтобы определить, доступ к каким пользователям в подписке отключен, используйте переключатель ExpandPrincipalGroups.</span><span class="sxs-lookup"><span data-stu-id="b4800-142">To determine what access is denied for a particular user in the subscription, use the ExpandPrincipalGroups switch.</span></span>
<span data-ttu-id="b4800-143">При этом будут перечисляться все запрещенные назначения, которые назначены пользователю, а также группам, в которые он входит.</span><span class="sxs-lookup"><span data-stu-id="b4800-143">This will list all deny assignments assigned to the user, and to the groups that the user is member of.</span></span>

## <span data-ttu-id="b4800-144">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b4800-144">EXAMPLES</span></span>

### <span data-ttu-id="b4800-145">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b4800-145">Example 1</span></span>

<span data-ttu-id="b4800-146">Список всех запрещенных заданий в подписке</span><span class="sxs-lookup"><span data-stu-id="b4800-146">List all deny assignments in the subscription</span></span>

```
PS C:\> Get-AzDenyAssignment
Id                      : 22704996-fbd0-4ab1-8625-722d897825d2
DenyAssignmentName      : Test deny assignment 1
Description             : Test deny assignment for PS cmdlets
Actions                 : {foo/*}
NotActions              : {foo/*/read}
DataActions             : {foo/*}
NotDataActions          : {}
Scope                   : /subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f
DoNotApplyToChildScopes : False
Principals              : {
                          DisplayName:  All Principals
                          ObjectType:   SystemDefined
                          ObjectId:     00000000-0000-0000-0000-000000000000
                          }
ExcludePrincipals       : {
                          DisplayName:  testuser
                          ObjectType:   User
                          ObjectId:     f8d526a0-54eb-4941-ae69-ebf4a334d0f0
                          }
IsSystemProtected       : True

Id                      : 43af7d0c-0bf8-407f-96c0-96a29d076431
DenyAssignmentName      : Test deny assignment 2
Description             : Test deny assignment for PS cmdlets
Actions                 : {foo/*}
NotActions              : {foo/*/read}
DataActions             : {foo/*}
NotDataActions          : {}
Scope                   : /subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourcegroups/testRG
DoNotApplyToChildScopes : False
Principals              : {
                          DisplayName:  testuser
                          ObjectType:   User
                          ObjectId:     f8d526a0-54eb-4941-ae69-ebf4a334d0f0
                          ,
                          DisplayName:  PowershellTestingApp
                          ObjectType:   ServicePrincipal
                          ObjectId:     f2dc21ac-702a-4bde-a4ce-146edf751d81
                          }
ExcludePrincipals       : {}
IsSystemProtected       : True
```

### <span data-ttu-id="b4800-147">Пример 2</span><span class="sxs-lookup"><span data-stu-id="b4800-147">Example 2</span></span>

<span data-ttu-id="b4800-148">Все отступные назначения, присвоенные пользователю, в john.doe@contoso.com области testRG и выше.</span><span class="sxs-lookup"><span data-stu-id="b4800-148">Gets all deny assignments made to user john.doe@contoso.com at the scope testRG and above.</span></span>

```
PS C:\> Get-AzDenyAssignment -ResourceGroupName testRG -SignInName john.doe@contoso.com

Id                      : 22704996-fbd0-4ab1-8625-722d897825d2
DenyAssignmentName      : Test deny assignment 1
Description             : Test deny assignment for PS cmdlets
Actions                 : {foo/*}
NotActions              : {foo/*/read}
DataActions             : {foo/*}
NotDataActions          : {}
Scope                   : /subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f
DoNotApplyToChildScopes : False
Principals              : {
                          DisplayName:  john.doe
                          ObjectType:   User
                          ObjectId:     f8d526a0-54eb-4941-ae69-ebf4a334d0f0
                          }
ExcludePrincipals       : {}
IsSystemProtected       : True

Id                      : 43af7d0c-0bf8-407f-96c0-96a29d076431
DenyAssignmentName      : Test deny assignment
Description             : Test deny assignment for PS cmdlets
Actions                 : {foo/*}
NotActions              : {foo/*/read}
DataActions             : {foo/*}
NotDataActions          : {}
Scope                   : /subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourcegroups/testRG
DoNotApplyToChildScopes : False
Principals              : {
                          DisplayName:  john.doe
                          ObjectType:   User
                          ObjectId:     f8d526a0-54eb-4941-ae69-ebf4a334d0f0
                          ,
                          DisplayName:  PowershellTestingApp
                          ObjectType:   ServicePrincipal
                          ObjectId:     f2dc21ac-702a-4bde-a4ce-146edf751d81
                          }
ExcludePrincipals       : {}
IsSystemProtected       : True
```

### <span data-ttu-id="b4800-149">Пример 3</span><span class="sxs-lookup"><span data-stu-id="b4800-149">Example 3</span></span>

<span data-ttu-id="b4800-150">Получает все отступные назначения указанного директора-службы</span><span class="sxs-lookup"><span data-stu-id="b4800-150">Gets all deny assignments of the specified service principal</span></span>

```
PS C:\> Get-AzDenyAssignment -ServicePrincipalName 'http://testapp1.com'

Id                      : 43af7d0c-0bf8-407f-96c0-96a29d076431
DenyAssignmentName      : Test deny assignment 1
Description             : Test deny assignment for PS cmdlets
Actions                 : {foo/*}
NotActions              : {foo/*/read}
DataActions             : {foo/*}
NotDataActions          : {}
Scope                   : /subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourcegroups/testRG
DoNotApplyToChildScopes : False
Principals              : {
                          DisplayName:  TestApp
                          ObjectType:   ServicePrincipal
                          ObjectId:     f2dc21ac-702a-4bde-a4ce-146edf751d81
                          }
ExcludePrincipals       : {}
IsSystemProtected       : True

Id                      : 94e3d9da-3700-4113-aab4-15f6c173d794
DenyAssignmentName      : Test deny assignment 2
Description             : Test deny assignment for PS cmdlets
Actions                 : {foo/*}
NotActions              : {foo/*/read}
DataActions             : {foo/*}
NotDataActions          : {}
Scope                   : /subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/testRG/providers/Microsoft.Web/sites/site1
DoNotApplyToChildScopes : False
Principals              : {
                          DisplayName:  testuser
                          ObjectType:   User
                          ObjectId:     f8d526a0-54eb-4941-ae69-ebf4a334d0f0
                          ,
                          DisplayName:  TestApp
                          ObjectType:   ServicePrincipal
                          ObjectId:     f2dc21ac-702a-4bde-a4ce-146edf751d81
                          }
ExcludePrincipals       : {}
IsSystemProtected       : True
```

### <span data-ttu-id="b4800-151">Пример 4</span><span class="sxs-lookup"><span data-stu-id="b4800-151">Example 4</span></span>

<span data-ttu-id="b4800-152">Возможность ото всех заданий в области веб-сайта site1.</span><span class="sxs-lookup"><span data-stu-id="b4800-152">Gets deny assignments at the 'site1' website scope.</span></span>

```
PS C:\> Get-AzDenyAssignment -Scope '/subscriptions/96231a05-34ce-4eb4-aa6a-70759cbb5e83/resourcegroups/testRG/providers/Microsoft.Web/sites/site1'

Id                      : 43af7d0c-0bf8-407f-96c0-96a29d076431
DenyAssignmentName      : Test deny assignment 1
Description             : Test deny assignment for PS cmdlets
Actions                 : {foo/*}
NotActions              : {foo/*/read}
DataActions             : {foo/*}
NotDataActions          : {}
Scope                   : /subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourcegroups/testRG
DoNotApplyToChildScopes : False
Principals              : {
                          DisplayName:  testuser
                          ObjectType:   User
                          ObjectId:     f8d526a0-54eb-4941-ae69-ebf4a334d0f0
                          }
ExcludePrincipals       : {}
IsSystemProtected       : True

Id                      : 94e3d9da-3700-4113-aab4-15f6c173d794
DenyAssignmentName      : Test deny assignment 2
Description             : Test deny assignment for PS cmdlets
Actions                 : {foo/*}
NotActions              : {foo/*/read}
DataActions             : {foo/*}
NotDataActions          : {}
Scope                   : /subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/testRG/providers/Microsoft.Web/sites/site1
DoNotApplyToChildScopes : False
Principals              : {
                          DisplayName:  testuser
                          ObjectType:   User
                          ObjectId:     f8d526a0-54eb-4941-ae69-ebf4a334d0f0
                          ,
                          DisplayName:  TestApp
                          ObjectType:   ServicePrincipal
                          ObjectId:     f2dc21ac-702a-4bde-a4ce-146edf751d81
                          }
ExcludePrincipals       : {}
IsSystemProtected       : True
```

## <span data-ttu-id="b4800-153">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b4800-153">PARAMETERS</span></span>

### <span data-ttu-id="b4800-154">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4800-154">-DefaultProfile</span></span>
<span data-ttu-id="b4800-155">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b4800-155">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b4800-156">-DenyAssignmentName</span><span class="sxs-lookup"><span data-stu-id="b4800-156">-DenyAssignmentName</span></span>
<span data-ttu-id="b4800-157">Имя запретного задания.</span><span class="sxs-lookup"><span data-stu-id="b4800-157">Name of the deny assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: DenyAssignmentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4800-158">-ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="b4800-158">-ExpandPrincipalGroups</span></span>
<span data-ttu-id="b4800-159">Если задан соответствующий пункт, возвращается запрет на назначение, непосредственно назначенное пользователю и группам, участником которых является пользователь (в пути).</span><span class="sxs-lookup"><span data-stu-id="b4800-159">If specified, returns deny assignments directly assigned to the user and to the groups of which the user is a member (transitively).</span></span>
<span data-ttu-id="b4800-160">Поддерживается только для основного пользователя.</span><span class="sxs-lookup"><span data-stu-id="b4800-160">Supported only for a user principal.</span></span>

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

### <span data-ttu-id="b4800-161">-Id</span><span class="sxs-lookup"><span data-stu-id="b4800-161">-Id</span></span>
<span data-ttu-id="b4800-162">Запретить ид задания.</span><span class="sxs-lookup"><span data-stu-id="b4800-162">Deny assignment id.</span></span>

```yaml
Type: System.Guid
Parameter Sets: DenyAssignmentIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4800-163">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="b4800-163">-ObjectId</span></span>
<span data-ttu-id="b4800-164">ОбъектId Azure AD пользователя, группы или директора службы.</span><span class="sxs-lookup"><span data-stu-id="b4800-164">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>
<span data-ttu-id="b4800-165">Фильтрует все отфильтрованные назначения, присвоенные указанному основному заданию.</span><span class="sxs-lookup"><span data-stu-id="b4800-165">Filters all deny assignments that are made to the specified principal.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: ObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ScopeWithObjectIdParameterSet
Aliases: PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4800-166">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="b4800-166">-ParentResource</span></span>
<span data-ttu-id="b4800-167">Родительский ресурс в иерархии ресурса, указанного с помощью параметра ResourceName.</span><span class="sxs-lookup"><span data-stu-id="b4800-167">The parent resource in the hierarchy of the resource specified using ResourceName parameter.</span></span>
<span data-ttu-id="b4800-168">Используется в сочетании с параметрами ResourceGroupName, ResourceType и ResourceName.</span><span class="sxs-lookup"><span data-stu-id="b4800-168">Must be used in conjunction with ResourceGroupName, ResourceType, and ResourceName parameters.</span></span>

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

### <span data-ttu-id="b4800-169">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4800-169">-ResourceGroupName</span></span>
<span data-ttu-id="b4800-170">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b4800-170">The resource group name.</span></span>
<span data-ttu-id="b4800-171">В списках не указаны назначения, эффективные для указанной группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b4800-171">Lists deny assignments that are effective at the specified resource group.</span></span>
<span data-ttu-id="b4800-172">При использовании в сочетании с параметрами ResourceName, ResourceType и ParentResource список команд не может запретить назначение ресурсов в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b4800-172">When used in conjunction with ResourceName, ResourceType, and ParentResource parameters, the command lists deny assignments effective at resources within the resource group.</span></span>

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

### <span data-ttu-id="b4800-173">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="b4800-173">-ResourceName</span></span>
<span data-ttu-id="b4800-174">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="b4800-174">The resource name.</span></span>
<span data-ttu-id="b4800-175">Например, storageaccountprod.</span><span class="sxs-lookup"><span data-stu-id="b4800-175">For e.g. storageaccountprod.</span></span>
<span data-ttu-id="b4800-176">Используется в сочетании с параметрами ResourceGroupName, ResourceType и (необязательно)ParentResource.</span><span class="sxs-lookup"><span data-stu-id="b4800-176">Must be used in conjunction with ResourceGroupName, ResourceType, and (optionally)ParentResource parameters.</span></span>

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

### <span data-ttu-id="b4800-177">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="b4800-177">-ResourceType</span></span>
<span data-ttu-id="b4800-178">Тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="b4800-178">The resource type.</span></span>
<span data-ttu-id="b4800-179">Например, Microsoft.Network/virtualNetworks.</span><span class="sxs-lookup"><span data-stu-id="b4800-179">For e.g. Microsoft.Network/virtualNetworks.</span></span>
<span data-ttu-id="b4800-180">Используется в сочетании с параметрами ResourceGroupName, ResourceName и (необязательно)ParentResource.</span><span class="sxs-lookup"><span data-stu-id="b4800-180">Must be used in conjunction with ResourceGroupName, ResourceName, and (optionally)ParentResource parameters.</span></span>

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

### <span data-ttu-id="b4800-181">-Scope</span><span class="sxs-lookup"><span data-stu-id="b4800-181">-Scope</span></span>
<span data-ttu-id="b4800-182">Область назначения роли.</span><span class="sxs-lookup"><span data-stu-id="b4800-182">The Scope of the role assignment.</span></span>
<span data-ttu-id="b4800-183">В формате относительного URI.</span><span class="sxs-lookup"><span data-stu-id="b4800-183">In the format of relative URI.</span></span>
<span data-ttu-id="b4800-184">Например, /subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG.</span><span class="sxs-lookup"><span data-stu-id="b4800-184">For e.g. /subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG.</span></span>
<span data-ttu-id="b4800-185">Оно должно начинаться с "/subscriptions/{id}".</span><span class="sxs-lookup"><span data-stu-id="b4800-185">It must start with "/subscriptions/{id}".</span></span>
<span data-ttu-id="b4800-186">Все командные фильтры отфильтруют все не те назначения, которые эффективны в этой области.</span><span class="sxs-lookup"><span data-stu-id="b4800-186">The command filters all deny assignments that are effective at that scope.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, DenyAssignmentIdParameterSet, DenyAssignmentNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### <span data-ttu-id="b4800-187">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="b4800-187">-ServicePrincipalName</span></span>
<span data-ttu-id="b4800-188">ServicePrincipalName основной услуги.</span><span class="sxs-lookup"><span data-stu-id="b4800-188">The ServicePrincipalName of the service principal.</span></span>
<span data-ttu-id="b4800-189">Фильтрует все отфильтрованные назначения, которые были присвоены указанному приложению Azure AD.</span><span class="sxs-lookup"><span data-stu-id="b4800-189">Filters all deny assignments that are made to the specified Azure AD application.</span></span>

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

### <span data-ttu-id="b4800-190">-SignInName</span><span class="sxs-lookup"><span data-stu-id="b4800-190">-SignInName</span></span>
<span data-ttu-id="b4800-191">Адрес электронной почты или имя директора пользователя.</span><span class="sxs-lookup"><span data-stu-id="b4800-191">The email address or the user principal name of the user.</span></span>
<span data-ttu-id="b4800-192">Фильтрует все запретные назначения, сделанные указанному пользователю.</span><span class="sxs-lookup"><span data-stu-id="b4800-192">Filters all deny assignments that are made to the specified user.</span></span>

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

### <span data-ttu-id="b4800-193">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4800-193">CommonParameters</span></span>
<span data-ttu-id="b4800-194">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4800-194">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4800-195">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b4800-195">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4800-196">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b4800-196">INPUTS</span></span>

### <span data-ttu-id="b4800-197">System.Guid</span><span class="sxs-lookup"><span data-stu-id="b4800-197">System.Guid</span></span>

### <span data-ttu-id="b4800-198">System.String</span><span class="sxs-lookup"><span data-stu-id="b4800-198">System.String</span></span>

## <span data-ttu-id="b4800-199">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b4800-199">OUTPUTS</span></span>

### <span data-ttu-id="b4800-200">Microsoft.Azure.Commands.Resources.Models.Authorization.PSDenyAssignment</span><span class="sxs-lookup"><span data-stu-id="b4800-200">Microsoft.Azure.Commands.Resources.Models.Authorization.PSDenyAssignment</span></span>

## <span data-ttu-id="b4800-201">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b4800-201">NOTES</span></span>
<span data-ttu-id="b4800-202">Ключевые слова: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span><span class="sxs-lookup"><span data-stu-id="b4800-202">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="b4800-203">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b4800-203">RELATED LINKS</span></span>