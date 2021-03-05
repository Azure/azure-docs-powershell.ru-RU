---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: E460D108-2BF9-4F57-AF3D-13868DC73EA0
online version: https://docs.microsoft.com/powershell/module/az.resources/new-azroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzRoleAssignment.md
ms.openlocfilehash: b21d265d507c1ff508c5db68094a65b54257931a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973523"
---
# <span data-ttu-id="94374-101">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="94374-101">New-AzRoleAssignment</span></span>

## <span data-ttu-id="94374-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94374-102">SYNOPSIS</span></span>
<span data-ttu-id="94374-103">Назначает указанную роль СРБ указанной основной в указанной области.</span><span class="sxs-lookup"><span data-stu-id="94374-103">Assigns the specified RBAC role to the specified principal, at the specified scope.</span></span>

## <span data-ttu-id="94374-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="94374-104">SYNTAX</span></span>

### <span data-ttu-id="94374-105">EmptyParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="94374-105">EmptyParameterSet (Default)</span></span>
```
New-AzRoleAssignment -ObjectId <String> [-Scope <String>] -RoleDefinitionName <String> [-Description <String>]
 [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94374-106">ResourceGroupWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="94374-106">ResourceGroupWithObjectIdParameterSet</span></span>
```
New-AzRoleAssignment -ObjectId <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-Description <String>] [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94374-107">ResourceWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="94374-107">ResourceWithObjectIdParameterSet</span></span>
```
New-AzRoleAssignment -ObjectId <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-Description <String>]
 [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94374-108">RoleIdWithScopeAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="94374-108">RoleIdWithScopeAndObjectIdParameterSet</span></span>
```
New-AzRoleAssignment -ObjectId <String> -Scope <String> [-Description <String>] [-Condition <String>]
 [-ConditionVersion <String>] -RoleDefinitionId <Guid> [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94374-109">ResourceGroupWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="94374-109">ResourceGroupWithSignInNameParameterSet</span></span>
```
New-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-Description <String>] [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94374-110">ResourceWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="94374-110">ResourceWithSignInNameParameterSet</span></span>
```
New-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-Description <String>]
 [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94374-111">ScopeWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="94374-111">ScopeWithSignInNameParameterSet</span></span>
```
New-AzRoleAssignment -SignInName <String> [-Scope <String>] -RoleDefinitionName <String>
 [-Description <String>] [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94374-112">ResourceGroupWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="94374-112">ResourceGroupWithSPNParameterSet</span></span>
```
New-AzRoleAssignment -ApplicationId <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-Description <String>] [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94374-113">ResourceWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="94374-113">ResourceWithSPNParameterSet</span></span>
```
New-AzRoleAssignment -ApplicationId <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-Description <String>]
 [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94374-114">ScopeWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="94374-114">ScopeWithSPNParameterSet</span></span>
```
New-AzRoleAssignment -ApplicationId <String> [-Scope <String>] -RoleDefinitionName <String>
 [-Description <String>] [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94374-115">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="94374-115">InputFileParameterSet</span></span>
```
New-AzRoleAssignment -InputFile <String> [-AllowDelegation] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="94374-116">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="94374-116">DESCRIPTION</span></span>
<span data-ttu-id="94374-117">Чтобы предоставить New-AzRoleAssignment доступ, используйте команду "Доступ".</span><span class="sxs-lookup"><span data-stu-id="94374-117">Use the New-AzRoleAssignment command to grant access.</span></span>
<span data-ttu-id="94374-118">Access предоставляется путем назначения им соответствующей роли RBAC в нужной области.</span><span class="sxs-lookup"><span data-stu-id="94374-118">Access is granted by assigning the appropriate RBAC role to them at the right scope.</span></span>
<span data-ttu-id="94374-119">Чтобы предоставить доступ ко всей подписке, назначьте роль в области подписки.</span><span class="sxs-lookup"><span data-stu-id="94374-119">To grant access to the entire subscription, assign a role at the subscription scope.</span></span>
<span data-ttu-id="94374-120">Чтобы предоставить доступ определенной группе ресурсов в рамках подписки, назначьте роль в ее области.</span><span class="sxs-lookup"><span data-stu-id="94374-120">To grant access to a specific resource group within a subscription, assign a role at the resource group scope.</span></span>
<span data-ttu-id="94374-121">Необходимо у указывается тема задания.</span><span class="sxs-lookup"><span data-stu-id="94374-121">The subject of the assignment must be specified.</span></span>
<span data-ttu-id="94374-122">Чтобы указать пользователя, используйте параметры SignInName или Azure AD ObjectId.</span><span class="sxs-lookup"><span data-stu-id="94374-122">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="94374-123">Чтобы указать группу безопасности, используйте параметр Azure AD ObjectId.</span><span class="sxs-lookup"><span data-stu-id="94374-123">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="94374-124">Чтобы указать приложение Azure AD, используйте параметры ApplicationId или ObjectId.</span><span class="sxs-lookup"><span data-stu-id="94374-124">And to specify an Azure AD application, use ApplicationId or ObjectId parameters.</span></span>
<span data-ttu-id="94374-125">Роль, которая должна быть назначена, должна быть указана с помощью параметра RoleDefinitionName.</span><span class="sxs-lookup"><span data-stu-id="94374-125">The role that is being assigned must be specified using the RoleDefinitionName parameter.</span></span>
<span data-ttu-id="94374-126">Может быть указана область, для которой предоставляется доступ.</span><span class="sxs-lookup"><span data-stu-id="94374-126">The scope at which access is being granted may be specified.</span></span>
<span data-ttu-id="94374-127">По умолчанию выбранная подписка.</span><span class="sxs-lookup"><span data-stu-id="94374-127">It defaults to the selected subscription.</span></span> <span data-ttu-id="94374-128">Область задания можно у определяет с помощью одного из следующих сочетаний параметров a.</span><span class="sxs-lookup"><span data-stu-id="94374-128">The scope of the assignment can be specified using one of the following parameter combinations a.</span></span>
<span data-ttu-id="94374-129">Область: это вся полнейская область, начиная с \<subscriptionId\> /subscriptions/b.</span><span class="sxs-lookup"><span data-stu-id="94374-129">Scope - This is the fully qualified scope starting with /subscriptions/\<subscriptionId\> b.</span></span>
<span data-ttu-id="94374-130">ResourceGroupName — предоставление доступа к указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="94374-130">ResourceGroupName - to grant access to the specified resource group.</span></span>
<span data-ttu-id="94374-131">в.</span><span class="sxs-lookup"><span data-stu-id="94374-131">c.</span></span>
<span data-ttu-id="94374-132">ResourceName, ResourceType, ResourceGroupName и (необязательно) ParentResource, чтобы указать определенный ресурс в группе ресурсов для предоставления доступа.</span><span class="sxs-lookup"><span data-stu-id="94374-132">ResourceName, ResourceType, ResourceGroupName and (optionally) ParentResource - to specify a particular resource within a resource group to grant access to.</span></span>

## <span data-ttu-id="94374-133">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="94374-133">EXAMPLES</span></span>

### <span data-ttu-id="94374-134">Пример 1</span><span class="sxs-lookup"><span data-stu-id="94374-134">Example 1</span></span>
```
PS C:\> New-AzRoleAssignment -ResourceGroupName rg1 -SignInName allen.young@live.com -RoleDefinitionName Reader -AllowDelegation
```

<span data-ttu-id="94374-135">Предоставление пользователю доступа к роли "Читатель" в области группы ресурсов, где назначение ролей доступно для делегирования</span><span class="sxs-lookup"><span data-stu-id="94374-135">Grant Reader role access to a user at a resource group scope with the Role Assignment being available for delegation</span></span>

### <span data-ttu-id="94374-136">Пример 2</span><span class="sxs-lookup"><span data-stu-id="94374-136">Example 2</span></span>
```
PS C:\> Get-AzADGroup -SearchString "Christine Koch Team"

          DisplayName                    Type                           Id
          -----------                    ----                           --------
          Christine Koch Team                                           2f9d4375-cbf1-48e8-83c9-2a0be4cb33fb

PS C:\> New-AzRoleAssignment -ObjectId 2f9d4375-cbf1-48e8-83c9-2a0be4cb33fb -RoleDefinitionName Contributor  -ResourceGroupName rg1
```

<span data-ttu-id="94374-137">Предоставление доступа группе безопасности</span><span class="sxs-lookup"><span data-stu-id="94374-137">Grant access to a security group</span></span>

### <span data-ttu-id="94374-138">Пример 3</span><span class="sxs-lookup"><span data-stu-id="94374-138">Example 3</span></span>
```
PS C:\> New-AzRoleAssignment -SignInName john.doe@contoso.com -RoleDefinitionName Owner -Scope "/subscriptions/86f81fc3-b00f-48cd-8218-3879f51ff362/resourcegroups/rg1/providers/Microsoft.Web/sites/site1"
```

<span data-ttu-id="94374-139">Предоставление пользователю доступа на ресурсе (веб-сайте)</span><span class="sxs-lookup"><span data-stu-id="94374-139">Grant access to a user at a resource (website)</span></span>

### <span data-ttu-id="94374-140">Пример 4</span><span class="sxs-lookup"><span data-stu-id="94374-140">Example 4</span></span>
```
PS C:\> New-AzRoleAssignment -ObjectId 5ac84765-1c8c-4994-94b2-629461bd191b -RoleDefinitionName "Virtual Machine Contributor" -ResourceName Devices-Engineering-ProjectRND -ResourceType Microsoft.Network/virtualNetworks/subnets -ParentResource virtualNetworks/VNET-EASTUS-01 -ResourceGroupName Network
```

<span data-ttu-id="94374-141">Предоставление доступа группе во вложенной сети (подсети)</span><span class="sxs-lookup"><span data-stu-id="94374-141">Grant access to a group at a nested resource (subnet)</span></span>

### <span data-ttu-id="94374-142">Пример 5</span><span class="sxs-lookup"><span data-stu-id="94374-142">Example 5</span></span>
```
PS C:\> $servicePrincipal = New-AzADServicePrincipal -DisplayName "testServiceprincipal"
PS C:\> New-AzRoleAssignment -RoleDefinitionName "Reader" -ApplicationId $servicePrincipal.ApplicationId
```

<span data-ttu-id="94374-143">Предоставление доступа читателю к основной службе</span><span class="sxs-lookup"><span data-stu-id="94374-143">Grant reader access to a service principal</span></span>

## <span data-ttu-id="94374-144">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="94374-144">PARAMETERS</span></span>

### <span data-ttu-id="94374-145">-AllowDelegation</span><span class="sxs-lookup"><span data-stu-id="94374-145">-AllowDelegation</span></span>
<span data-ttu-id="94374-146">Флаг делегирования при создании назначения роли.</span><span class="sxs-lookup"><span data-stu-id="94374-146">The delegation flag while creating a Role assignment.</span></span>

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

### <span data-ttu-id="94374-147">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="94374-147">-ApplicationId</span></span>
<span data-ttu-id="94374-148">The Application ID of the ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="94374-148">The Application ID of the ServicePrincipal</span></span>

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

### <span data-ttu-id="94374-149">-Condition</span><span class="sxs-lookup"><span data-stu-id="94374-149">-Condition</span></span>
<span data-ttu-id="94374-150">Условие, которое будет применено к roleAssignment.</span><span class="sxs-lookup"><span data-stu-id="94374-150">Condition to be applied to the RoleAssignment.</span></span>

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

### <span data-ttu-id="94374-151">-ConditionVersion</span><span class="sxs-lookup"><span data-stu-id="94374-151">-ConditionVersion</span></span>
<span data-ttu-id="94374-152">Версия условия.</span><span class="sxs-lookup"><span data-stu-id="94374-152">Version of the condition.</span></span>

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

### <span data-ttu-id="94374-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94374-153">-DefaultProfile</span></span>
<span data-ttu-id="94374-154">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="94374-154">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="94374-155">-Description</span><span class="sxs-lookup"><span data-stu-id="94374-155">-Description</span></span>
<span data-ttu-id="94374-156">Краткое описание назначения роли.</span><span class="sxs-lookup"><span data-stu-id="94374-156">Brief description of the role assignment.</span></span>

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

### <span data-ttu-id="94374-157">-InputFile</span><span class="sxs-lookup"><span data-stu-id="94374-157">-InputFile</span></span>
<span data-ttu-id="94374-158">Path to role assignment json</span><span class="sxs-lookup"><span data-stu-id="94374-158">Path to role assignment json</span></span>

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

### <span data-ttu-id="94374-159">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="94374-159">-ObjectId</span></span>
<span data-ttu-id="94374-160">Объект Azure AD пользователя, группы или основной службы.</span><span class="sxs-lookup"><span data-stu-id="94374-160">Azure AD Objectid of the user, group or service principal.</span></span>

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

### <span data-ttu-id="94374-161">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="94374-161">-ParentResource</span></span>
<span data-ttu-id="94374-162">Родительский ресурс в иерархии (из ресурса, указанного с помощью параметра ResourceName).</span><span class="sxs-lookup"><span data-stu-id="94374-162">The parent resource in the hierarchy(of the resource specified using ResourceName parameter).</span></span>
<span data-ttu-id="94374-163">Используется только в сочетании с параметрами ResourceGroupName, ResourceType и ResourceName для создания иерархической области в форме относительного URI, определяемого ресурсом.</span><span class="sxs-lookup"><span data-stu-id="94374-163">Should only be  used in conjunction with ResourceGroupName, ResourceType and ResourceName parameters to construct a hierarchical scope in the form of a relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="94374-164">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94374-164">-ResourceGroupName</span></span>
<span data-ttu-id="94374-165">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="94374-165">The resource group name.</span></span>
<span data-ttu-id="94374-166">Создает назначение, эффективное для указанной группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="94374-166">Creates an assignment that is effective at the specified resource group.</span></span>
<span data-ttu-id="94374-167">При использовании в сочетании с параметрами ResourceName, ResourceType и (необязательно)ParentResource команда формирует иерархическую область в виде относительного URI, определяемого ресурсом.</span><span class="sxs-lookup"><span data-stu-id="94374-167">When used in conjunction with ResourceName, ResourceType and (optionally)ParentResource parameters, the command constructs a hierarchical scope in the form of a relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="94374-168">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="94374-168">-ResourceName</span></span>
<span data-ttu-id="94374-169">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="94374-169">The resource name.</span></span>
<span data-ttu-id="94374-170">Например, storageaccountprod.</span><span class="sxs-lookup"><span data-stu-id="94374-170">For e.g. storageaccountprod.</span></span>
<span data-ttu-id="94374-171">Используется только в сочетании с параметрами ResourceGroupName, ResourceType и (необязательно)ParentResource для создания иерархической области в форме относительного URI, определяемого ресурсом.</span><span class="sxs-lookup"><span data-stu-id="94374-171">Should only be used in conjunction with ResourceGroupName, ResourceType and (optionally)ParentResource parameters to construct a hierarchical scope in the form of a  relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="94374-172">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="94374-172">-ResourceType</span></span>
<span data-ttu-id="94374-173">Тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="94374-173">The resource type.</span></span>
<span data-ttu-id="94374-174">Например, Microsoft.Network/virtualNetworks.</span><span class="sxs-lookup"><span data-stu-id="94374-174">For e.g. Microsoft.Network/virtualNetworks.</span></span>
<span data-ttu-id="94374-175">Используется только в сочетании с параметрами ResourceGroupName, ResourceName и (необязательно)ParentResource для создания иерархической области в форме относительного URI, определяемого ресурсом.</span><span class="sxs-lookup"><span data-stu-id="94374-175">Should only be used in conjunction with ResourceGroupName, ResourceName and (optionally)ParentResource parameters to construct a hierarchical scope in  the form of a relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="94374-176">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="94374-176">-RoleDefinitionId</span></span>
<span data-ttu-id="94374-177">ИД роли СДБ, которая должна быть назначена основному.</span><span class="sxs-lookup"><span data-stu-id="94374-177">Id of the RBAC role that needs to be assigned to the principal.</span></span>

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

### <span data-ttu-id="94374-178">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="94374-178">-RoleDefinitionName</span></span>
<span data-ttu-id="94374-179">Имя роли СДВ, которая должна быть назначена основной роли, например "Читатель", "Участник", "Виртуальный администратор сети" и т. д.</span><span class="sxs-lookup"><span data-stu-id="94374-179">Name of the RBAC role that needs to be assigned to the principal i.e. Reader, Contributor, Virtual Network Administrator, etc.</span></span>

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

### <span data-ttu-id="94374-180">-Scope</span><span class="sxs-lookup"><span data-stu-id="94374-180">-Scope</span></span>
<span data-ttu-id="94374-181">Область назначения роли.</span><span class="sxs-lookup"><span data-stu-id="94374-181">The Scope of the role assignment.</span></span>
<span data-ttu-id="94374-182">В формате относительного URI.</span><span class="sxs-lookup"><span data-stu-id="94374-182">In the format of relative URI.</span></span>
<span data-ttu-id="94374-183">Например: "/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG".</span><span class="sxs-lookup"><span data-stu-id="94374-183">For e.g. "/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG".</span></span>
<span data-ttu-id="94374-184">Если не указано, будет создаваться назначение роли на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="94374-184">If not specified, will create the role assignment at subscription level.</span></span>
<span data-ttu-id="94374-185">Если указано, оно должно начинаться с "/subscriptions/{id}".</span><span class="sxs-lookup"><span data-stu-id="94374-185">If specified, it should start with "/subscriptions/{id}".</span></span>

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

### <span data-ttu-id="94374-186">-SignInName</span><span class="sxs-lookup"><span data-stu-id="94374-186">-SignInName</span></span>
<span data-ttu-id="94374-187">Адрес электронной почты или имя директора пользователя.</span><span class="sxs-lookup"><span data-stu-id="94374-187">The email address or the user principal name of the user.</span></span>

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

### <span data-ttu-id="94374-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94374-188">CommonParameters</span></span>
<span data-ttu-id="94374-189">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94374-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94374-190">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="94374-190">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94374-191">INPUTS</span><span class="sxs-lookup"><span data-stu-id="94374-191">INPUTS</span></span>

### <span data-ttu-id="94374-192">System.String</span><span class="sxs-lookup"><span data-stu-id="94374-192">System.String</span></span>

### <span data-ttu-id="94374-193">System.Guid</span><span class="sxs-lookup"><span data-stu-id="94374-193">System.Guid</span></span>

## <span data-ttu-id="94374-194">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="94374-194">OUTPUTS</span></span>

### <span data-ttu-id="94374-195">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="94374-195">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>

## <span data-ttu-id="94374-196">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="94374-196">NOTES</span></span>
<span data-ttu-id="94374-197">Ключевые слова: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span><span class="sxs-lookup"><span data-stu-id="94374-197">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="94374-198">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="94374-198">RELATED LINKS</span></span>

[<span data-ttu-id="94374-199">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="94374-199">Get-AzRoleAssignment</span></span>](./Get-AzRoleAssignment.md)

[<span data-ttu-id="94374-200">Remove-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="94374-200">Remove-AzRoleAssignment</span></span>](./Remove-AzRoleAssignment.md)

[<span data-ttu-id="94374-201">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="94374-201">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)
