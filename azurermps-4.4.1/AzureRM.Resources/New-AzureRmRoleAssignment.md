---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: E460D108-2BF9-4F57-AF3D-13868DC73EA0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmRoleAssignment.md
ms.openlocfilehash: c3988727e8afd54dddea9719c348222c41f47503
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565169"
---
# <span data-ttu-id="69fe6-101">New-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="69fe6-101">New-AzureRmRoleAssignment</span></span>

## <span data-ttu-id="69fe6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="69fe6-102">SYNOPSIS</span></span>
<span data-ttu-id="69fe6-103">Назначает указанную роль RBAC указанному участнику в заданной области.</span><span class="sxs-lookup"><span data-stu-id="69fe6-103">Assigns the specified RBAC role to the specified principal, at the specified scope.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="69fe6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="69fe6-104">SYNTAX</span></span>

### <span data-ttu-id="69fe6-105">EmptyParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="69fe6-105">EmptyParameterSet (Default)</span></span>
```
New-AzureRmRoleAssignment -ObjectId <Guid> -Scope <String> -RoleDefinitionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="69fe6-106">ResourceGroupWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="69fe6-106">ResourceGroupWithObjectIdParameterSet</span></span>
```
New-AzureRmRoleAssignment -ObjectId <Guid> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="69fe6-107">ResourceWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="69fe6-107">ResourceWithObjectIdParameterSet</span></span>
```
New-AzureRmRoleAssignment -ObjectId <Guid> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="69fe6-108">ScopeWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="69fe6-108">ScopeWithObjectIdParameterSet</span></span>
```
New-AzureRmRoleAssignment -ObjectId <Guid> [-Scope <String>] -RoleDefinitionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="69fe6-109">RoleIdWithScopeAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="69fe6-109">RoleIdWithScopeAndObjectIdParameterSet</span></span>
```
New-AzureRmRoleAssignment -ObjectId <Guid> -Scope <String> -RoleDefinitionId <Guid>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="69fe6-110">ResourceGroupWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="69fe6-110">ResourceGroupWithSignInNameParameterSet</span></span>
```
New-AzureRmRoleAssignment -SignInName <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="69fe6-111">ResourceWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="69fe6-111">ResourceWithSignInNameParameterSet</span></span>
```
New-AzureRmRoleAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="69fe6-112">ScopeWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="69fe6-112">ScopeWithSignInNameParameterSet</span></span>
```
New-AzureRmRoleAssignment -SignInName <String> [-Scope <String>] -RoleDefinitionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="69fe6-113">ResourceGroupWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="69fe6-113">ResourceGroupWithSPNParameterSet</span></span>
```
New-AzureRmRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String>
 -RoleDefinitionName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="69fe6-114">ResourceWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="69fe6-114">ResourceWithSPNParameterSet</span></span>
```
New-AzureRmRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="69fe6-115">ScopeWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="69fe6-115">ScopeWithSPNParameterSet</span></span>
```
New-AzureRmRoleAssignment -ServicePrincipalName <String> [-Scope <String>] -RoleDefinitionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="69fe6-116">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="69fe6-116">DESCRIPTION</span></span>
<span data-ttu-id="69fe6-117">Для предоставления доступа используйте команду "New-AzureRMRoleAssignment".</span><span class="sxs-lookup"><span data-stu-id="69fe6-117">Use the New-AzureRMRoleAssignment command to grant access.</span></span>
<span data-ttu-id="69fe6-118">Доступ предоставляется путем назначения им соответствующей роли RBAC в области справа.</span><span class="sxs-lookup"><span data-stu-id="69fe6-118">Access is granted by assigning the appropriate RBAC role to them at the right scope.</span></span>
<span data-ttu-id="69fe6-119">Чтобы предоставить доступ ко всей подписке, назначьте роль в области подписки.</span><span class="sxs-lookup"><span data-stu-id="69fe6-119">To grant access to the entire subscription, assign a role at the subscription scope.</span></span>
<span data-ttu-id="69fe6-120">Чтобы предоставить доступ к определенной группе ресурсов в рамках подписки, назначьте роль в области "Группа ресурсов".</span><span class="sxs-lookup"><span data-stu-id="69fe6-120">To grant access to a specific resource group within a subscription, assign a role at the resource group scope.</span></span>

<span data-ttu-id="69fe6-121">Необходимо указать тему назначения.</span><span class="sxs-lookup"><span data-stu-id="69fe6-121">The subject of the assignment must be specified.</span></span>
<span data-ttu-id="69fe6-122">Чтобы указать пользователя, используйте параметры SignInName или Azure AD ObjectId.</span><span class="sxs-lookup"><span data-stu-id="69fe6-122">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="69fe6-123">Чтобы указать группу безопасности, используйте параметр Azure AD ObjectId.</span><span class="sxs-lookup"><span data-stu-id="69fe6-123">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="69fe6-124">Чтобы указать приложение Azure AD, используйте параметры "ИД" или "ObjectId".</span><span class="sxs-lookup"><span data-stu-id="69fe6-124">And to specify an Azure AD application, use ServicePrincipalName or ObjectId parameters.</span></span>

<span data-ttu-id="69fe6-125">Назначаемая роль должна быть указана с помощью параметра RoleDefinitionName.</span><span class="sxs-lookup"><span data-stu-id="69fe6-125">The role that is being assigned must be specified using the RoleDefinitionName parameter.</span></span>

<span data-ttu-id="69fe6-126">Может быть указана область, для которой предоставляется доступ.</span><span class="sxs-lookup"><span data-stu-id="69fe6-126">The scope at which access is being granted may be specified.</span></span>
<span data-ttu-id="69fe6-127">По умолчанию используется выбранная подписка.</span><span class="sxs-lookup"><span data-stu-id="69fe6-127">It defaults to the selected subscription.</span></span> <span data-ttu-id="69fe6-128">Область назначения может быть указана с помощью одного из следующих сочетаний параметров a.</span><span class="sxs-lookup"><span data-stu-id="69fe6-128">The scope of the assignment can be specified using one of the following parameter combinations a.</span></span>
<span data-ttu-id="69fe6-129">Scope — это полностью определенная область, начиная с/Subscriptions/ \<subscriptionId\> b.</span><span class="sxs-lookup"><span data-stu-id="69fe6-129">Scope - This is the fully qualified scope starting with /subscriptions/\<subscriptionId\> b.</span></span>
<span data-ttu-id="69fe6-130">ResourceGroupName — предоставление доступа к указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="69fe6-130">ResourceGroupName - to grant access to the specified resource group.</span></span>
<span data-ttu-id="69fe6-131">c++.</span><span class="sxs-lookup"><span data-stu-id="69fe6-131">c.</span></span>
<span data-ttu-id="69fe6-132">ResourceName, ResourceType, ResourceGroupName и (необязательно) ParentResource — указание определенного ресурса в группе ресурсов для предоставления доступа.</span><span class="sxs-lookup"><span data-stu-id="69fe6-132">ResourceName, ResourceType, ResourceGroupName and (optionally) ParentResource - to specify a particular resource within a resource group to grant access to.</span></span>

## <span data-ttu-id="69fe6-133">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="69fe6-133">EXAMPLES</span></span>

### <span data-ttu-id="69fe6-134">--------------------------Пример 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="69fe6-134">--------------------------  Example 1  --------------------------</span></span>
```
PS C:\> New-AzureRmRoleAssignment -ResourceGroupName rg1 -SignInName allen.young@live.com -RoleDefinitionName Reader
```

<span data-ttu-id="69fe6-135">Предоставление пользователю доступа к роли "читатель" на уровне группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="69fe6-135">Grant Reader role access to a user at a resource group scope</span></span>

### <span data-ttu-id="69fe6-136">--------------------------Пример 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="69fe6-136">--------------------------  Example 2  --------------------------</span></span>
```
PS C:\> Get-AzureRMADGroup -SearchString "Christine Koch Team"

          DisplayName                    Type                           ObjectId
          -----------                    ----                           --------
          Christine Koch Team                                           2f9d4375-cbf1-48e8-83c9-2a0be4cb33fb

PS C:\> New-AzureRmRoleAssignment -ObjectId 2f9d4375-cbf1-48e8-83c9-2a0be4cb33fb -RoleDefinitionName Contributor  -ResourceGroupName rg1
```

<span data-ttu-id="69fe6-137">Предоставление доступа группе безопасности</span><span class="sxs-lookup"><span data-stu-id="69fe6-137">Grant access to a security group</span></span>

### <span data-ttu-id="69fe6-138">--------------------------Пример 3--------------------------</span><span class="sxs-lookup"><span data-stu-id="69fe6-138">--------------------------  Example 3  --------------------------</span></span>
```
PS C:\> New-AzureRmRoleAssignment -SignInName john.doe@contoso.com -RoleDefinitionName Owner -Scope "/subscriptions/86f81fc3-b00f-48cd-8218-3879f51ff362/resourcegroups/rg1/providers/Microsoft.Web/sites/site1"
```

<span data-ttu-id="69fe6-139">Предоставление доступа пользователю на ресурсе (веб-сайте)</span><span class="sxs-lookup"><span data-stu-id="69fe6-139">Grant access to a user at a resource (website)</span></span>

### <span data-ttu-id="69fe6-140">--------------------------Пример 4--------------------------</span><span class="sxs-lookup"><span data-stu-id="69fe6-140">--------------------------  Example 4  --------------------------</span></span>
```
PS C:\> New-AzureRMRoleAssignment -ObjectId 5ac84765-1c8c-4994-94b2-629461bd191b -RoleDefinitionName "Virtual Machine Contributor" -ResourceName Devices-Engineering-ProjectRND -ResourceType Microsoft.Network/virtualNetworks/subnets -ParentResource virtualNetworks/VNET-EASTUS-01 -ResourceGroupName Network
```

<span data-ttu-id="69fe6-141">Предоставление доступа к группе во вложенном ресурсе (подсеть)</span><span class="sxs-lookup"><span data-stu-id="69fe6-141">Grant access to a group at a nested resource (subnet)</span></span>

## <span data-ttu-id="69fe6-142">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="69fe6-142">PARAMETERS</span></span>

### <span data-ttu-id="69fe6-143">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="69fe6-143">-ObjectId</span></span>
<span data-ttu-id="69fe6-144">Azure AD ObjectID для пользователя, группы или участника-службы.</span><span class="sxs-lookup"><span data-stu-id="69fe6-144">Azure AD Objectid of the user, group or service principal.</span></span>

```yaml
Type: System.Guid
Parameter Sets: EmptyParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ScopeWithObjectIdParameterSet, RoleIdWithScopeAndObjectIdParameterSet
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69fe6-145">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="69fe6-145">-ParentResource</span></span>
<span data-ttu-id="69fe6-146">Родительский ресурс в иерархии (ресурс, указанный с помощью параметра ResourceName).</span><span class="sxs-lookup"><span data-stu-id="69fe6-146">The parent resource in the hierarchy(of the resource specified using ResourceName parameter).</span></span>
<span data-ttu-id="69fe6-147">Следует использовать только в сочетании с параметрами ResourceGroupName, ResourceType и ResourceName для создания иерархической области в форме относительного URI, определяющего ресурс.</span><span class="sxs-lookup"><span data-stu-id="69fe6-147">Should only be  used in conjunction with ResourceGroupName, ResourceType and ResourceName parameters to construct a hierarchical scope in the form of a relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="69fe6-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69fe6-148">-ResourceGroupName</span></span>
<span data-ttu-id="69fe6-149">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="69fe6-149">The resource group name.</span></span>
<span data-ttu-id="69fe6-150">Создание задания, действующего в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="69fe6-150">Creates an assignment that is effective at the specified resource group.</span></span>
<span data-ttu-id="69fe6-151">При использовании в сочетании с ResourceName, ResourceType и (необязательно) параметрами ParentResource команда создает иерархическую область в форме относительного URI, который определяет ресурс.</span><span class="sxs-lookup"><span data-stu-id="69fe6-151">When used in conjunction with ResourceName, ResourceType and (optionally)ParentResource parameters, the command constructs a hierarchical scope in the form of a relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="69fe6-152">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="69fe6-152">-ResourceName</span></span>
<span data-ttu-id="69fe6-153">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="69fe6-153">The resource name.</span></span>
<span data-ttu-id="69fe6-154">Например, storageaccountprod.</span><span class="sxs-lookup"><span data-stu-id="69fe6-154">For e.g. storageaccountprod.</span></span>
<span data-ttu-id="69fe6-155">Следует использовать только в сочетании с ResourceGroupName, ResourceType и (необязательно) параметрами ParentResource для создания иерархической области в форме относительного URI, определяющего ресурс.</span><span class="sxs-lookup"><span data-stu-id="69fe6-155">Should only be used in conjunction with ResourceGroupName, ResourceType and (optionally)ParentResource parameters to construct a hierarchical scope in the form of a  relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="69fe6-156">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="69fe6-156">-ResourceType</span></span>
<span data-ttu-id="69fe6-157">Тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="69fe6-157">The resource type.</span></span>
<span data-ttu-id="69fe6-158">Для таких, например, Microsoft. Network/virtualNetworks.</span><span class="sxs-lookup"><span data-stu-id="69fe6-158">For e.g. Microsoft.Network/virtualNetworks.</span></span>
<span data-ttu-id="69fe6-159">Следует использовать только в сочетании с ResourceGroupName, ResourceName и (необязательно) параметрами ParentResource для создания иерархической области в форме относительного URI, определяющего ресурс.</span><span class="sxs-lookup"><span data-stu-id="69fe6-159">Should only be used in conjunction with ResourceGroupName, ResourceName and (optionally)ParentResource parameters to construct a hierarchical scope in  the form of a relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="69fe6-160">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="69fe6-160">-RoleDefinitionId</span></span>
<span data-ttu-id="69fe6-161">Идентификатор роли RBAC, который должен быть назначен участнику.</span><span class="sxs-lookup"><span data-stu-id="69fe6-161">Id of the RBAC role that needs to be assigned to the principal.</span></span>

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

### <span data-ttu-id="69fe6-162">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="69fe6-162">-RoleDefinitionName</span></span>
<span data-ttu-id="69fe6-163">Имя роли RBAC, которое должно быть назначено для участника, например читатель, участник, Администратор виртуальной сети и т. д.</span><span class="sxs-lookup"><span data-stu-id="69fe6-163">Name of the RBAC role that needs to be assigned to the principal i.e. Reader, Contributor, Virtual Network Administrator, etc.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ScopeWithObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69fe6-164">-Scope</span><span class="sxs-lookup"><span data-stu-id="69fe6-164">-Scope</span></span>
<span data-ttu-id="69fe6-165">Область назначения роли.</span><span class="sxs-lookup"><span data-stu-id="69fe6-165">The Scope of the role assignment.</span></span>
<span data-ttu-id="69fe6-166">В формате относительных URI.</span><span class="sxs-lookup"><span data-stu-id="69fe6-166">In the format of relative URI.</span></span>
<span data-ttu-id="69fe6-167">Например, "/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG".</span><span class="sxs-lookup"><span data-stu-id="69fe6-167">For e.g. "/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG".</span></span>
<span data-ttu-id="69fe6-168">Если не указано, будет создано назначение ролей на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="69fe6-168">If not specified, will create the role assignment at subscription level.</span></span>
<span data-ttu-id="69fe6-169">Если указан, она должна начинаться с "/Subscriptions/{ID}".</span><span class="sxs-lookup"><span data-stu-id="69fe6-169">If specified, it should start with "/subscriptions/{id}".</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, RoleIdWithScopeAndObjectIdParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ScopeWithObjectIdParameterSet, ScopeWithSignInNameParameterSet, ScopeWithSPNParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69fe6-170">-Намерено</span><span class="sxs-lookup"><span data-stu-id="69fe6-170">-ServicePrincipalName</span></span>
<span data-ttu-id="69fe6-171">Значение программного приложения Azure AD</span><span class="sxs-lookup"><span data-stu-id="69fe6-171">The ServicePrincipalName of the Azure AD application</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69fe6-172">-SignInName</span><span class="sxs-lookup"><span data-stu-id="69fe6-172">-SignInName</span></span>
<span data-ttu-id="69fe6-173">Адрес электронной почты или имя участника-пользователя.</span><span class="sxs-lookup"><span data-stu-id="69fe6-173">The email address or the user principal name of the user.</span></span>

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

### <span data-ttu-id="69fe6-174">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69fe6-174">-DefaultProfile</span></span>
<span data-ttu-id="69fe6-175">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="69fe6-175">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69fe6-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69fe6-176">CommonParameters</span></span>
<span data-ttu-id="69fe6-177">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="69fe6-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69fe6-178">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69fe6-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69fe6-179">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="69fe6-179">INPUTS</span></span>

## <span data-ttu-id="69fe6-180">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="69fe6-180">OUTPUTS</span></span>

### <span data-ttu-id="69fe6-181">Microsoft. Azure. Commands. Resources. Authorization. PSRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="69fe6-181">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>

## <span data-ttu-id="69fe6-182">Пуск</span><span class="sxs-lookup"><span data-stu-id="69fe6-182">NOTES</span></span>
<span data-ttu-id="69fe6-183">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, ресурс, группа, шаблон, развертывание</span><span class="sxs-lookup"><span data-stu-id="69fe6-183">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="69fe6-184">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="69fe6-184">RELATED LINKS</span></span>

[<span data-ttu-id="69fe6-185">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="69fe6-185">Get-AzureRmRoleAssignment</span></span>](./Get-AzureRmRoleAssignment.md)

[<span data-ttu-id="69fe6-186">Remove-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="69fe6-186">Remove-AzureRmRoleAssignment</span></span>](./Remove-AzureRmRoleAssignment.md)

[<span data-ttu-id="69fe6-187">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="69fe6-187">Get-AzureRmRoleDefinition</span></span>](./Get-AzureRmRoleDefinition.md)

