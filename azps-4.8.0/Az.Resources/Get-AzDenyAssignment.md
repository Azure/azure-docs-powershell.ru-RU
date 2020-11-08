---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdenyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDenyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDenyAssignment.md
ms.openlocfilehash: 22acfc03afa4758c44d6c6f02ac1d734c90a806b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235456"
---
# <span data-ttu-id="0c343-101">Get-AzDenyAssignment</span><span class="sxs-lookup"><span data-stu-id="0c343-101">Get-AzDenyAssignment</span></span>

## <span data-ttu-id="0c343-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0c343-102">SYNOPSIS</span></span>
<span data-ttu-id="0c343-103">Список запрета заданий в заданной области в Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="0c343-103">Lists Azure RBAC deny assignments at the specified scope.</span></span>
<span data-ttu-id="0c343-104">По умолчанию выводится список всех запрещенных заданий в выбранной подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="0c343-104">By default it lists all deny assignments in the selected Azure subscription.</span></span>
<span data-ttu-id="0c343-105">Используйте соответствующие параметры для списка отказа от назначения определенному пользователю или для включения в список запрещенных назначений для определенной группы или ресурса.</span><span class="sxs-lookup"><span data-stu-id="0c343-105">Use respective parameters to list deny assignments to a specific user, or to list deny assignments on a specific resource group or resource.</span></span>

## <span data-ttu-id="0c343-106">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0c343-106">SYNTAX</span></span>

### <span data-ttu-id="0c343-107">EmptyParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0c343-107">EmptyParameterSet (Default)</span></span>
```
Get-AzDenyAssignment [-Scope <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0c343-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c343-108">ObjectIdParameterSet</span></span>
```
Get-AzDenyAssignment -ObjectId <Guid> [-ExpandPrincipalGroups] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0c343-109">ResourceGroupWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c343-109">ResourceGroupWithObjectIdParameterSet</span></span>
```
Get-AzDenyAssignment -ObjectId <Guid> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0c343-110">ResourceWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c343-110">ResourceWithObjectIdParameterSet</span></span>
```
Get-AzDenyAssignment -ObjectId <Guid> -ResourceGroupName <String> -ResourceName <String> -ResourceType <String>
 [-ParentResource <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0c343-111">ScopeWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c343-111">ScopeWithObjectIdParameterSet</span></span>
```
Get-AzDenyAssignment -ObjectId <Guid> -Scope <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0c343-112">ResourceGroupWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c343-112">ResourceGroupWithSignInNameParameterSet</span></span>
```
Get-AzDenyAssignment -SignInName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0c343-113">ResourceWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c343-113">ResourceWithSignInNameParameterSet</span></span>
```
Get-AzDenyAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0c343-114">ScopeWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c343-114">ScopeWithSignInNameParameterSet</span></span>
```
Get-AzDenyAssignment -SignInName <String> -Scope <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0c343-115">SignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c343-115">SignInNameParameterSet</span></span>
```
Get-AzDenyAssignment -SignInName <String> [-ExpandPrincipalGroups] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0c343-116">ResourceGroupWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c343-116">ResourceGroupWithSPNParameterSet</span></span>
```
Get-AzDenyAssignment -ServicePrincipalName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0c343-117">ResourceWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c343-117">ResourceWithSPNParameterSet</span></span>
```
Get-AzDenyAssignment -ServicePrincipalName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0c343-118">ScopeWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c343-118">ScopeWithSPNParameterSet</span></span>
```
Get-AzDenyAssignment -ServicePrincipalName <String> -Scope <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0c343-119">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c343-119">SPNParameterSet</span></span>
```
Get-AzDenyAssignment -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0c343-120">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c343-120">ResourceGroupParameterSet</span></span>
```
Get-AzDenyAssignment -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0c343-121">ResourceParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c343-121">ResourceParameterSet</span></span>
```
Get-AzDenyAssignment -ResourceGroupName <String> -ResourceName <String> -ResourceType <String>
 [-ParentResource <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0c343-122">ScopeParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c343-122">ScopeParameterSet</span></span>
```
Get-AzDenyAssignment -Scope <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0c343-123">DenyAssignmentIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c343-123">DenyAssignmentIdParameterSet</span></span>
```
Get-AzDenyAssignment [-Scope <String>] -Id <Guid> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0c343-124">DenyAssignmentNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c343-124">DenyAssignmentNameParameterSet</span></span>
```
Get-AzDenyAssignment [-Scope <String>] -DenyAssignmentName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0c343-125">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0c343-125">DESCRIPTION</span></span>
<span data-ttu-id="0c343-126">С помощью команды Get-AzDenyAssignment можно вывести список всех запрещенных назначений в области.</span><span class="sxs-lookup"><span data-stu-id="0c343-126">Use the Get-AzDenyAssignment command to list all deny assignments that are effective on a scope.</span></span>
<span data-ttu-id="0c343-127">При отсутствии каких бы то ни было параметров эта команда возвращает все назначения отказа, внесенные в подписку.</span><span class="sxs-lookup"><span data-stu-id="0c343-127">Without any parameters, this command returns all the deny assignments made under the subscription.</span></span>
<span data-ttu-id="0c343-128">Этот список можно фильтровать с помощью параметров фильтрации для участника, отклонить имя и область назначения.</span><span class="sxs-lookup"><span data-stu-id="0c343-128">This list can  be filtered using filtering parameters for principal, deny assignment name and scope.</span></span>
<span data-ttu-id="0c343-129">Чтобы указать пользователя, используйте параметры SignInName или Azure AD ObjectId.</span><span class="sxs-lookup"><span data-stu-id="0c343-129">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="0c343-130">Чтобы указать группу безопасности, используйте параметр Azure AD ObjectId.</span><span class="sxs-lookup"><span data-stu-id="0c343-130">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="0c343-131">Чтобы указать приложение Azure AD, используйте параметры "ИД" или "ObjectId".</span><span class="sxs-lookup"><span data-stu-id="0c343-131">And to specify an Azure AD application, use ServicePrincipalName or ObjectId parameters.</span></span>
<span data-ttu-id="0c343-132">Может быть указана область, в которой отказано в доступе.</span><span class="sxs-lookup"><span data-stu-id="0c343-132">The scope at which access is being denied may be specified.</span></span>
<span data-ttu-id="0c343-133">По умолчанию используется выбранная подписка.</span><span class="sxs-lookup"><span data-stu-id="0c343-133">It defaults to the selected subscription.</span></span>
<span data-ttu-id="0c343-134">Область назначения Deny может быть указана с помощью одного из следующих сочетаний параметров a.</span><span class="sxs-lookup"><span data-stu-id="0c343-134">The scope of the deny assignment can be specified using one of the following parameter combinations a.</span></span>
<span data-ttu-id="0c343-135">Scope — это полностью определенная область, начиная с/Subscriptions/ \<subscriptionId\> .</span><span class="sxs-lookup"><span data-stu-id="0c343-135">Scope - This is the fully qualified scope starting with /subscriptions/\<subscriptionId\>.</span></span>
<span data-ttu-id="0c343-136">Это позволит отклонять назначения, действующие в этой конкретной области, таким образом, чтобы отклонить назначения в этой области и более поздней.</span><span class="sxs-lookup"><span data-stu-id="0c343-136">This will filter deny assignments that are effective at that particular scope i.e. all deny assignments at that scope and above.</span></span>
<span data-ttu-id="0c343-137">байт.</span><span class="sxs-lookup"><span data-stu-id="0c343-137">b.</span></span>
<span data-ttu-id="0c343-138">ResourceGroupName — имя любой группы ресурсов в рамках подписки.</span><span class="sxs-lookup"><span data-stu-id="0c343-138">ResourceGroupName - Name of any resource group under the subscription.</span></span>
<span data-ttu-id="0c343-139">Это позволяет отфильтровать назначения, действующие в заданной группе ресурсов, т. е. все запретные назначения в этой области и более поздней.</span><span class="sxs-lookup"><span data-stu-id="0c343-139">This will filter assignments effective at the specified resource group i.e. all deny assignments at that scope and above.</span></span>
<span data-ttu-id="0c343-140">c++.</span><span class="sxs-lookup"><span data-stu-id="0c343-140">c.</span></span>
<span data-ttu-id="0c343-141">ResourceName, ResourceType, ResourceGroupName и (необязательно) ParentResource — определяет конкретный ресурс в подписке и будет фильтровать отказы на назначения, действующие в этой области ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0c343-141">ResourceName, ResourceType, ResourceGroupName and (optionally) ParentResource - Identifies a particular resource under the subscription and will filter deny assignments effective at that resource scope.</span></span>
<span data-ttu-id="0c343-142">Чтобы определить отказ в доступе для определенного пользователя в подписке, используйте параметр ExpandPrincipalGroups.</span><span class="sxs-lookup"><span data-stu-id="0c343-142">To determine what access is denied for a particular user in the subscription, use the ExpandPrincipalGroups switch.</span></span>
<span data-ttu-id="0c343-143">Будут перечислены все отказы назначения, назначенные пользователю, и группы, в которые входит пользователь.</span><span class="sxs-lookup"><span data-stu-id="0c343-143">This will list all deny assignments assigned to the user, and to the groups that the user is member of.</span></span>

## <span data-ttu-id="0c343-144">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0c343-144">EXAMPLES</span></span>

### <span data-ttu-id="0c343-145">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0c343-145">Example 1</span></span>

<span data-ttu-id="0c343-146">Список всех запрещенных заданий в подписке</span><span class="sxs-lookup"><span data-stu-id="0c343-146">List all deny assignments in the subscription</span></span>

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

### <span data-ttu-id="0c343-147">Пример 2</span><span class="sxs-lookup"><span data-stu-id="0c343-147">Example 2</span></span>

<span data-ttu-id="0c343-148">Возвращает все запрещенные назначения для пользователя john.doe@contoso.com в области testRG и более поздней.</span><span class="sxs-lookup"><span data-stu-id="0c343-148">Gets all deny assignments made to user john.doe@contoso.com at the scope testRG and above.</span></span>

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

### <span data-ttu-id="0c343-149">Пример 3</span><span class="sxs-lookup"><span data-stu-id="0c343-149">Example 3</span></span>

<span data-ttu-id="0c343-150">Возвращает все запрещенные назначения для указанного субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="0c343-150">Gets all deny assignments of the specified service principal</span></span>

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

### <span data-ttu-id="0c343-151">Пример 4</span><span class="sxs-lookup"><span data-stu-id="0c343-151">Example 4</span></span>

<span data-ttu-id="0c343-152">Возвращает назначение для отклонения в области веб-сайта "site1".</span><span class="sxs-lookup"><span data-stu-id="0c343-152">Gets deny assignments at the 'site1' website scope.</span></span>

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

## <span data-ttu-id="0c343-153">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0c343-153">PARAMETERS</span></span>

### <span data-ttu-id="0c343-154">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c343-154">-DefaultProfile</span></span>
<span data-ttu-id="0c343-155">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="0c343-155">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0c343-156">-DenyAssignmentName</span><span class="sxs-lookup"><span data-stu-id="0c343-156">-DenyAssignmentName</span></span>
<span data-ttu-id="0c343-157">Имя назначения отказа.</span><span class="sxs-lookup"><span data-stu-id="0c343-157">Name of the deny assignment.</span></span>

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

### <span data-ttu-id="0c343-158">-ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="0c343-158">-ExpandPrincipalGroups</span></span>
<span data-ttu-id="0c343-159">Если задано значение, возвращает запрет на назначения, непосредственно назначенные пользователю, и группам, участником которых является пользователь (транзитивно).</span><span class="sxs-lookup"><span data-stu-id="0c343-159">If specified, returns deny assignments directly assigned to the user and to the groups of which the user is a member (transitively).</span></span>
<span data-ttu-id="0c343-160">Поддерживается только для участника-пользователя.</span><span class="sxs-lookup"><span data-stu-id="0c343-160">Supported only for a user principal.</span></span>

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

### <span data-ttu-id="0c343-161">-ID</span><span class="sxs-lookup"><span data-stu-id="0c343-161">-Id</span></span>
<span data-ttu-id="0c343-162">Отклонить код назначения.</span><span class="sxs-lookup"><span data-stu-id="0c343-162">Deny assignment id.</span></span>

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

### <span data-ttu-id="0c343-163">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="0c343-163">-ObjectId</span></span>
<span data-ttu-id="0c343-164">ИД служб Azure AD ObjectId для пользователя, группы или участника-службы.</span><span class="sxs-lookup"><span data-stu-id="0c343-164">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>
<span data-ttu-id="0c343-165">Фильтрует все запрещающие задания, которые выполняются для указанного участника.</span><span class="sxs-lookup"><span data-stu-id="0c343-165">Filters all deny assignments that are made to the specified principal.</span></span>

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

### <span data-ttu-id="0c343-166">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="0c343-166">-ParentResource</span></span>
<span data-ttu-id="0c343-167">Родительский ресурс в иерархии ресурса, указанный с помощью параметра ResourceName.</span><span class="sxs-lookup"><span data-stu-id="0c343-167">The parent resource in the hierarchy of the resource specified using ResourceName parameter.</span></span>
<span data-ttu-id="0c343-168">Необходимо использовать в сочетании с параметрами ResourceGroupName, ResourceType и ResourceName.</span><span class="sxs-lookup"><span data-stu-id="0c343-168">Must be used in conjunction with ResourceGroupName, ResourceType, and ResourceName parameters.</span></span>

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

### <span data-ttu-id="0c343-169">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c343-169">-ResourceGroupName</span></span>
<span data-ttu-id="0c343-170">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0c343-170">The resource group name.</span></span>
<span data-ttu-id="0c343-171">Список запретов назначений, которые действуют в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0c343-171">Lists deny assignments that are effective at the specified resource group.</span></span>
<span data-ttu-id="0c343-172">При использовании в сочетании с параметрами ResourceName, ResourceType и ParentResource команда перечисляет запрещает задания, действующие на ресурсах в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0c343-172">When used in conjunction with ResourceName, ResourceType, and ParentResource parameters, the command lists deny assignments effective at resources within the resource group.</span></span>

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

### <span data-ttu-id="0c343-173">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="0c343-173">-ResourceName</span></span>
<span data-ttu-id="0c343-174">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="0c343-174">The resource name.</span></span>
<span data-ttu-id="0c343-175">Например, storageaccountprod.</span><span class="sxs-lookup"><span data-stu-id="0c343-175">For e.g. storageaccountprod.</span></span>
<span data-ttu-id="0c343-176">Необходимо использовать в сочетании с ResourceGroupName, ResourceType и (необязательно) параметрами ParentResource.</span><span class="sxs-lookup"><span data-stu-id="0c343-176">Must be used in conjunction with ResourceGroupName, ResourceType, and (optionally)ParentResource parameters.</span></span>

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

### <span data-ttu-id="0c343-177">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="0c343-177">-ResourceType</span></span>
<span data-ttu-id="0c343-178">Тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="0c343-178">The resource type.</span></span>
<span data-ttu-id="0c343-179">Для таких, например, Microsoft. Network/virtualNetworks.</span><span class="sxs-lookup"><span data-stu-id="0c343-179">For e.g. Microsoft.Network/virtualNetworks.</span></span>
<span data-ttu-id="0c343-180">Необходимо использовать в сочетании с ResourceGroupName, ResourceName и (необязательно) параметрами ParentResource.</span><span class="sxs-lookup"><span data-stu-id="0c343-180">Must be used in conjunction with ResourceGroupName, ResourceName, and (optionally)ParentResource parameters.</span></span>

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

### <span data-ttu-id="0c343-181">-Scope</span><span class="sxs-lookup"><span data-stu-id="0c343-181">-Scope</span></span>
<span data-ttu-id="0c343-182">Область назначения роли.</span><span class="sxs-lookup"><span data-stu-id="0c343-182">The Scope of the role assignment.</span></span>
<span data-ttu-id="0c343-183">В формате относительных URI.</span><span class="sxs-lookup"><span data-stu-id="0c343-183">In the format of relative URI.</span></span>
<span data-ttu-id="0c343-184">Например,/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG.</span><span class="sxs-lookup"><span data-stu-id="0c343-184">For e.g. /subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG.</span></span>
<span data-ttu-id="0c343-185">Оно должно начинаться с "/Subscriptions/{ID}".</span><span class="sxs-lookup"><span data-stu-id="0c343-185">It must start with "/subscriptions/{id}".</span></span>
<span data-ttu-id="0c343-186">Команда фильтрует все запрещенные назначения, действующие в этой области.</span><span class="sxs-lookup"><span data-stu-id="0c343-186">The command filters all deny assignments that are effective at that scope.</span></span>

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

### <span data-ttu-id="0c343-187">-Намерено</span><span class="sxs-lookup"><span data-stu-id="0c343-187">-ServicePrincipalName</span></span>
<span data-ttu-id="0c343-188">Значение параметра безопасности участника-службы.</span><span class="sxs-lookup"><span data-stu-id="0c343-188">The ServicePrincipalName of the service principal.</span></span>
<span data-ttu-id="0c343-189">Фильтрует все запрещенные назначения, выполненные в указанном приложении Azure AD.</span><span class="sxs-lookup"><span data-stu-id="0c343-189">Filters all deny assignments that are made to the specified Azure AD application.</span></span>

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

### <span data-ttu-id="0c343-190">-SignInName</span><span class="sxs-lookup"><span data-stu-id="0c343-190">-SignInName</span></span>
<span data-ttu-id="0c343-191">Адрес электронной почты или имя участника-пользователя.</span><span class="sxs-lookup"><span data-stu-id="0c343-191">The email address or the user principal name of the user.</span></span>
<span data-ttu-id="0c343-192">Фильтрует все запрещающие задания, которые выполняются указанному пользователю.</span><span class="sxs-lookup"><span data-stu-id="0c343-192">Filters all deny assignments that are made to the specified user.</span></span>

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

### <span data-ttu-id="0c343-193">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c343-193">CommonParameters</span></span>
<span data-ttu-id="0c343-194">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0c343-194">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c343-195">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0c343-195">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c343-196">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0c343-196">INPUTS</span></span>

### <span data-ttu-id="0c343-197">System. GUID</span><span class="sxs-lookup"><span data-stu-id="0c343-197">System.Guid</span></span>

### <span data-ttu-id="0c343-198">System. String</span><span class="sxs-lookup"><span data-stu-id="0c343-198">System.String</span></span>

## <span data-ttu-id="0c343-199">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0c343-199">OUTPUTS</span></span>

### <span data-ttu-id="0c343-200">Microsoft.Azure.Commands.Resources.Models.Authorization.PSDenyAssignment</span><span class="sxs-lookup"><span data-stu-id="0c343-200">Microsoft.Azure.Commands.Resources.Models.Authorization.PSDenyAssignment</span></span>

## <span data-ttu-id="0c343-201">Пуск</span><span class="sxs-lookup"><span data-stu-id="0c343-201">NOTES</span></span>
<span data-ttu-id="0c343-202">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, ресурс, группа, шаблон, развертывание</span><span class="sxs-lookup"><span data-stu-id="0c343-202">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="0c343-203">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0c343-203">RELATED LINKS</span></span>