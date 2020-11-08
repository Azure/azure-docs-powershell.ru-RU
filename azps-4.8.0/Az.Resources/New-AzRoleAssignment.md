---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: E460D108-2BF9-4F57-AF3D-13868DC73EA0
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzRoleAssignment.md
ms.openlocfilehash: 2ec39bc66b3b027cb7b5ef9dda09734f8aaf457a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235436"
---
# <span data-ttu-id="ae333-101">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="ae333-101">New-AzRoleAssignment</span></span>

## <span data-ttu-id="ae333-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ae333-102">SYNOPSIS</span></span>
<span data-ttu-id="ae333-103">Назначает указанную роль RBAC указанному участнику в заданной области.</span><span class="sxs-lookup"><span data-stu-id="ae333-103">Assigns the specified RBAC role to the specified principal, at the specified scope.</span></span>

## <span data-ttu-id="ae333-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ae333-104">SYNTAX</span></span>

### <span data-ttu-id="ae333-105">EmptyParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ae333-105">EmptyParameterSet (Default)</span></span>
```
New-AzRoleAssignment -ObjectId <String> [-Scope <String>] -RoleDefinitionName <String> [-Description <String>]
 [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae333-106">ResourceGroupWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ae333-106">ResourceGroupWithObjectIdParameterSet</span></span>
```
New-AzRoleAssignment -ObjectId <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-Description <String>] [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae333-107">ResourceWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ae333-107">ResourceWithObjectIdParameterSet</span></span>
```
New-AzRoleAssignment -ObjectId <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-Description <String>]
 [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae333-108">RoleIdWithScopeAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ae333-108">RoleIdWithScopeAndObjectIdParameterSet</span></span>
```
New-AzRoleAssignment -ObjectId <String> -Scope <String> [-Description <String>] [-Condition <String>]
 [-ConditionVersion <String>] -RoleDefinitionId <Guid> [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae333-109">ResourceGroupWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ae333-109">ResourceGroupWithSignInNameParameterSet</span></span>
```
New-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-Description <String>] [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae333-110">ResourceWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ae333-110">ResourceWithSignInNameParameterSet</span></span>
```
New-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-Description <String>]
 [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae333-111">ScopeWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ae333-111">ScopeWithSignInNameParameterSet</span></span>
```
New-AzRoleAssignment -SignInName <String> [-Scope <String>] -RoleDefinitionName <String>
 [-Description <String>] [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae333-112">ResourceGroupWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="ae333-112">ResourceGroupWithSPNParameterSet</span></span>
```
New-AzRoleAssignment -ApplicationId <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-Description <String>] [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae333-113">ResourceWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="ae333-113">ResourceWithSPNParameterSet</span></span>
```
New-AzRoleAssignment -ApplicationId <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-Description <String>]
 [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae333-114">ScopeWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="ae333-114">ScopeWithSPNParameterSet</span></span>
```
New-AzRoleAssignment -ApplicationId <String> [-Scope <String>] -RoleDefinitionName <String>
 [-Description <String>] [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae333-115">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="ae333-115">InputFileParameterSet</span></span>
```
New-AzRoleAssignment -InputFile <String> [-AllowDelegation] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ae333-116">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ae333-116">DESCRIPTION</span></span>
<span data-ttu-id="ae333-117">Для предоставления доступа используйте команду "New-AzRoleAssignment".</span><span class="sxs-lookup"><span data-stu-id="ae333-117">Use the New-AzRoleAssignment command to grant access.</span></span>
<span data-ttu-id="ae333-118">Доступ предоставляется путем назначения им соответствующей роли RBAC в области справа.</span><span class="sxs-lookup"><span data-stu-id="ae333-118">Access is granted by assigning the appropriate RBAC role to them at the right scope.</span></span>
<span data-ttu-id="ae333-119">Чтобы предоставить доступ ко всей подписке, назначьте роль в области подписки.</span><span class="sxs-lookup"><span data-stu-id="ae333-119">To grant access to the entire subscription, assign a role at the subscription scope.</span></span>
<span data-ttu-id="ae333-120">Чтобы предоставить доступ к определенной группе ресурсов в рамках подписки, назначьте роль в области "Группа ресурсов".</span><span class="sxs-lookup"><span data-stu-id="ae333-120">To grant access to a specific resource group within a subscription, assign a role at the resource group scope.</span></span>
<span data-ttu-id="ae333-121">Необходимо указать тему назначения.</span><span class="sxs-lookup"><span data-stu-id="ae333-121">The subject of the assignment must be specified.</span></span>
<span data-ttu-id="ae333-122">Чтобы указать пользователя, используйте параметры SignInName или Azure AD ObjectId.</span><span class="sxs-lookup"><span data-stu-id="ae333-122">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="ae333-123">Чтобы указать группу безопасности, используйте параметр Azure AD ObjectId.</span><span class="sxs-lookup"><span data-stu-id="ae333-123">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="ae333-124">Чтобы указать приложение Azure AD, используйте параметры ApplicationId или ObjectId.</span><span class="sxs-lookup"><span data-stu-id="ae333-124">And to specify an Azure AD application, use ApplicationId or ObjectId parameters.</span></span>
<span data-ttu-id="ae333-125">Назначаемая роль должна быть указана с помощью параметра RoleDefinitionName.</span><span class="sxs-lookup"><span data-stu-id="ae333-125">The role that is being assigned must be specified using the RoleDefinitionName parameter.</span></span>
<span data-ttu-id="ae333-126">Может быть указана область, для которой предоставляется доступ.</span><span class="sxs-lookup"><span data-stu-id="ae333-126">The scope at which access is being granted may be specified.</span></span>
<span data-ttu-id="ae333-127">По умолчанию используется выбранная подписка.</span><span class="sxs-lookup"><span data-stu-id="ae333-127">It defaults to the selected subscription.</span></span> <span data-ttu-id="ae333-128">Область назначения может быть указана с помощью одного из следующих сочетаний параметров a.</span><span class="sxs-lookup"><span data-stu-id="ae333-128">The scope of the assignment can be specified using one of the following parameter combinations a.</span></span>
<span data-ttu-id="ae333-129">Scope — это полностью определенная область, начиная с/Subscriptions/ \<subscriptionId\> b.</span><span class="sxs-lookup"><span data-stu-id="ae333-129">Scope - This is the fully qualified scope starting with /subscriptions/\<subscriptionId\> b.</span></span>
<span data-ttu-id="ae333-130">ResourceGroupName — предоставление доступа к указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ae333-130">ResourceGroupName - to grant access to the specified resource group.</span></span>
<span data-ttu-id="ae333-131">c++.</span><span class="sxs-lookup"><span data-stu-id="ae333-131">c.</span></span>
<span data-ttu-id="ae333-132">ResourceName, ResourceType, ResourceGroupName и (необязательно) ParentResource — указание определенного ресурса в группе ресурсов для предоставления доступа.</span><span class="sxs-lookup"><span data-stu-id="ae333-132">ResourceName, ResourceType, ResourceGroupName and (optionally) ParentResource - to specify a particular resource within a resource group to grant access to.</span></span>

## <span data-ttu-id="ae333-133">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ae333-133">EXAMPLES</span></span>

### <span data-ttu-id="ae333-134">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ae333-134">Example 1</span></span>
```
PS C:\> New-AzRoleAssignment -ResourceGroupName rg1 -SignInName allen.young@live.com -RoleDefinitionName Reader -AllowDelegation
```

<span data-ttu-id="ae333-135">Предоставление пользователю доступа к роли "читатель" на уровне группы ресурсов с назначением роли, доступным для делегирования</span><span class="sxs-lookup"><span data-stu-id="ae333-135">Grant Reader role access to a user at a resource group scope with the Role Assignment being available for delegation</span></span>

### <span data-ttu-id="ae333-136">Пример 2</span><span class="sxs-lookup"><span data-stu-id="ae333-136">Example 2</span></span>
```
PS C:\> Get-AzADGroup -SearchString "Christine Koch Team"

          DisplayName                    Type                           Id
          -----------                    ----                           --------
          Christine Koch Team                                           2f9d4375-cbf1-48e8-83c9-2a0be4cb33fb

PS C:\> New-AzRoleAssignment -ObjectId 2f9d4375-cbf1-48e8-83c9-2a0be4cb33fb -RoleDefinitionName Contributor  -ResourceGroupName rg1
```

<span data-ttu-id="ae333-137">Предоставление доступа группе безопасности</span><span class="sxs-lookup"><span data-stu-id="ae333-137">Grant access to a security group</span></span>

### <span data-ttu-id="ae333-138">Пример 3</span><span class="sxs-lookup"><span data-stu-id="ae333-138">Example 3</span></span>
```
PS C:\> New-AzRoleAssignment -SignInName john.doe@contoso.com -RoleDefinitionName Owner -Scope "/subscriptions/86f81fc3-b00f-48cd-8218-3879f51ff362/resourcegroups/rg1/providers/Microsoft.Web/sites/site1"
```

<span data-ttu-id="ae333-139">Предоставление доступа пользователю на ресурсе (веб-сайте)</span><span class="sxs-lookup"><span data-stu-id="ae333-139">Grant access to a user at a resource (website)</span></span>

### <span data-ttu-id="ae333-140">Пример 4</span><span class="sxs-lookup"><span data-stu-id="ae333-140">Example 4</span></span>
```
PS C:\> New-AzRoleAssignment -ObjectId 5ac84765-1c8c-4994-94b2-629461bd191b -RoleDefinitionName "Virtual Machine Contributor" -ResourceName Devices-Engineering-ProjectRND -ResourceType Microsoft.Network/virtualNetworks/subnets -ParentResource virtualNetworks/VNET-EASTUS-01 -ResourceGroupName Network
```

<span data-ttu-id="ae333-141">Предоставление доступа к группе во вложенном ресурсе (подсеть)</span><span class="sxs-lookup"><span data-stu-id="ae333-141">Grant access to a group at a nested resource (subnet)</span></span>

### <span data-ttu-id="ae333-142">Пример 5</span><span class="sxs-lookup"><span data-stu-id="ae333-142">Example 5</span></span>
```
PS C:\> $servicePrincipal = New-AzADServicePrincipal -DisplayName "testServiceprincipal"
PS C:\> New-AzRoleAssignment -RoleDefinitionName "Reader" -ApplicationId $servicePrincipal.ApplicationId
```

<span data-ttu-id="ae333-143">Предоставление доступного для читателя участника-службы</span><span class="sxs-lookup"><span data-stu-id="ae333-143">Grant reader access to a service principal</span></span>

## <span data-ttu-id="ae333-144">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ae333-144">PARAMETERS</span></span>

### <span data-ttu-id="ae333-145">-AllowDelegation</span><span class="sxs-lookup"><span data-stu-id="ae333-145">-AllowDelegation</span></span>
<span data-ttu-id="ae333-146">Флаг делегирования при создании назначения роли.</span><span class="sxs-lookup"><span data-stu-id="ae333-146">The delegation flag while creating a Role assignment.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae333-147">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="ae333-147">-ApplicationId</span></span>
<span data-ttu-id="ae333-148">Идентификатор приложения для ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="ae333-148">The Application ID of the ServicePrincipal</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet
Aliases: SPN, ServicePrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae333-149">-Условие</span><span class="sxs-lookup"><span data-stu-id="ae333-149">-Condition</span></span>
<span data-ttu-id="ae333-150">Условие, применяемое к RoleAssignment.</span><span class="sxs-lookup"><span data-stu-id="ae333-150">Condition to be applied to the RoleAssignment.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, RoleIdWithScopeAndObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae333-151">-ConditionVersion</span><span class="sxs-lookup"><span data-stu-id="ae333-151">-ConditionVersion</span></span>
<span data-ttu-id="ae333-152">Версия условия.</span><span class="sxs-lookup"><span data-stu-id="ae333-152">Version of the condition.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, RoleIdWithScopeAndObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae333-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae333-153">-DefaultProfile</span></span>
<span data-ttu-id="ae333-154">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="ae333-154">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ae333-155">-Описание</span><span class="sxs-lookup"><span data-stu-id="ae333-155">-Description</span></span>
<span data-ttu-id="ae333-156">Краткое описание назначения роли.</span><span class="sxs-lookup"><span data-stu-id="ae333-156">Brief description of the role assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, RoleIdWithScopeAndObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae333-157">-InputFile</span><span class="sxs-lookup"><span data-stu-id="ae333-157">-InputFile</span></span>
<span data-ttu-id="ae333-158">Путь к файлу назначения роли JSON</span><span class="sxs-lookup"><span data-stu-id="ae333-158">Path to role assignment json</span></span>

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae333-159">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="ae333-159">-ObjectId</span></span>
<span data-ttu-id="ae333-160">Azure AD ObjectID для пользователя, группы или участника-службы.</span><span class="sxs-lookup"><span data-stu-id="ae333-160">Azure AD Objectid of the user, group or service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, RoleIdWithScopeAndObjectIdParameterSet
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae333-161">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="ae333-161">-ParentResource</span></span>
<span data-ttu-id="ae333-162">Родительский ресурс в иерархии (ресурс, указанный с помощью параметра ResourceName).</span><span class="sxs-lookup"><span data-stu-id="ae333-162">The parent resource in the hierarchy(of the resource specified using ResourceName parameter).</span></span>
<span data-ttu-id="ae333-163">Следует использовать только в сочетании с параметрами ResourceGroupName, ResourceType и ResourceName для создания иерархической области в форме относительного URI, определяющего ресурс.</span><span class="sxs-lookup"><span data-stu-id="ae333-163">Should only be  used in conjunction with ResourceGroupName, ResourceType and ResourceName parameters to construct a hierarchical scope in the form of a relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="ae333-164">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae333-164">-ResourceGroupName</span></span>
<span data-ttu-id="ae333-165">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ae333-165">The resource group name.</span></span>
<span data-ttu-id="ae333-166">Создание задания, действующего в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ae333-166">Creates an assignment that is effective at the specified resource group.</span></span>
<span data-ttu-id="ae333-167">При использовании в сочетании с ResourceName, ResourceType и (необязательно) параметрами ParentResource команда создает иерархическую область в форме относительного URI, который определяет ресурс.</span><span class="sxs-lookup"><span data-stu-id="ae333-167">When used in conjunction with ResourceName, ResourceType and (optionally)ParentResource parameters, the command constructs a hierarchical scope in the form of a relative URI that identifies a resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae333-168">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="ae333-168">-ResourceName</span></span>
<span data-ttu-id="ae333-169">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="ae333-169">The resource name.</span></span>
<span data-ttu-id="ae333-170">Например, storageaccountprod.</span><span class="sxs-lookup"><span data-stu-id="ae333-170">For e.g. storageaccountprod.</span></span>
<span data-ttu-id="ae333-171">Следует использовать только в сочетании с ResourceGroupName, ResourceType и (необязательно) параметрами ParentResource для создания иерархической области в форме относительного URI, определяющего ресурс.</span><span class="sxs-lookup"><span data-stu-id="ae333-171">Should only be used in conjunction with ResourceGroupName, ResourceType and (optionally)ParentResource parameters to construct a hierarchical scope in the form of a  relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="ae333-172">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="ae333-172">-ResourceType</span></span>
<span data-ttu-id="ae333-173">Тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="ae333-173">The resource type.</span></span>
<span data-ttu-id="ae333-174">Для таких, например, Microsoft. Network/virtualNetworks.</span><span class="sxs-lookup"><span data-stu-id="ae333-174">For e.g. Microsoft.Network/virtualNetworks.</span></span>
<span data-ttu-id="ae333-175">Следует использовать только в сочетании с ResourceGroupName, ResourceName и (необязательно) параметрами ParentResource для создания иерархической области в форме относительного URI, определяющего ресурс.</span><span class="sxs-lookup"><span data-stu-id="ae333-175">Should only be used in conjunction with ResourceGroupName, ResourceName and (optionally)ParentResource parameters to construct a hierarchical scope in  the form of a relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="ae333-176">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="ae333-176">-RoleDefinitionId</span></span>
<span data-ttu-id="ae333-177">Идентификатор роли RBAC, который должен быть назначен участнику.</span><span class="sxs-lookup"><span data-stu-id="ae333-177">Id of the RBAC role that needs to be assigned to the principal.</span></span>

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

### <span data-ttu-id="ae333-178">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="ae333-178">-RoleDefinitionName</span></span>
<span data-ttu-id="ae333-179">Имя роли RBAC, которое должно быть назначено для участника, например читатель, участник, Администратор виртуальной сети и т. д.</span><span class="sxs-lookup"><span data-stu-id="ae333-179">Name of the RBAC role that needs to be assigned to the principal i.e. Reader, Contributor, Virtual Network Administrator, etc.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae333-180">-Scope</span><span class="sxs-lookup"><span data-stu-id="ae333-180">-Scope</span></span>
<span data-ttu-id="ae333-181">Область назначения роли.</span><span class="sxs-lookup"><span data-stu-id="ae333-181">The Scope of the role assignment.</span></span>
<span data-ttu-id="ae333-182">В формате относительных URI.</span><span class="sxs-lookup"><span data-stu-id="ae333-182">In the format of relative URI.</span></span>
<span data-ttu-id="ae333-183">Например, "/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG".</span><span class="sxs-lookup"><span data-stu-id="ae333-183">For e.g. "/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG".</span></span>
<span data-ttu-id="ae333-184">Если не указано, будет создано назначение ролей на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="ae333-184">If not specified, will create the role assignment at subscription level.</span></span>
<span data-ttu-id="ae333-185">Если указан, она должна начинаться с "/Subscriptions/{ID}".</span><span class="sxs-lookup"><span data-stu-id="ae333-185">If specified, it should start with "/subscriptions/{id}".</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ScopeWithSignInNameParameterSet, ScopeWithSPNParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: RoleIdWithScopeAndObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae333-186">-SignInName</span><span class="sxs-lookup"><span data-stu-id="ae333-186">-SignInName</span></span>
<span data-ttu-id="ae333-187">Адрес электронной почты или имя участника-пользователя.</span><span class="sxs-lookup"><span data-stu-id="ae333-187">The email address or the user principal name of the user.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet
Aliases: Email, UserPrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae333-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae333-188">CommonParameters</span></span>
<span data-ttu-id="ae333-189">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ae333-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae333-190">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ae333-190">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae333-191">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ae333-191">INPUTS</span></span>

### <span data-ttu-id="ae333-192">System. String</span><span class="sxs-lookup"><span data-stu-id="ae333-192">System.String</span></span>

### <span data-ttu-id="ae333-193">System. GUID</span><span class="sxs-lookup"><span data-stu-id="ae333-193">System.Guid</span></span>

## <span data-ttu-id="ae333-194">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ae333-194">OUTPUTS</span></span>

### <span data-ttu-id="ae333-195">Microsoft. Azure. Commands. Resources. Authorization. PSRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="ae333-195">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>

## <span data-ttu-id="ae333-196">Пуск</span><span class="sxs-lookup"><span data-stu-id="ae333-196">NOTES</span></span>
<span data-ttu-id="ae333-197">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, ресурс, группа, шаблон, развертывание</span><span class="sxs-lookup"><span data-stu-id="ae333-197">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="ae333-198">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ae333-198">RELATED LINKS</span></span>

[<span data-ttu-id="ae333-199">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="ae333-199">Get-AzRoleAssignment</span></span>](./Get-AzRoleAssignment.md)

[<span data-ttu-id="ae333-200">Remove-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="ae333-200">Remove-AzRoleAssignment</span></span>](./Remove-AzRoleAssignment.md)

[<span data-ttu-id="ae333-201">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="ae333-201">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)
