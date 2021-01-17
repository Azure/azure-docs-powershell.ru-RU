---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/new-azmanagedservicesdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/New-AzManagedServicesDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/New-AzManagedServicesDefinition.md
ms.openlocfilehash: f8d2eded01e4816b99b71475aca896c697dd5ae0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98415476"
---
# <span data-ttu-id="b12fb-101">New-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="b12fb-101">New-AzManagedServicesDefinition</span></span>

## <span data-ttu-id="b12fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b12fb-102">SYNOPSIS</span></span>
<span data-ttu-id="b12fb-103">Создание или обновление определения регистрации.</span><span class="sxs-lookup"><span data-stu-id="b12fb-103">Creates or updates a registration definition.</span></span>

## <span data-ttu-id="b12fb-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b12fb-104">SYNTAX</span></span>

### <span data-ttu-id="b12fb-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b12fb-105">Default (Default)</span></span>
```
New-AzManagedServicesDefinition [-Name <String>] -DisplayName <String> -ManagedByTenantId <String>
 [-Description <String>] -PrincipalId <String> -RoleDefinitionId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b12fb-106">ByPlan</span><span class="sxs-lookup"><span data-stu-id="b12fb-106">ByPlan</span></span>
```
New-AzManagedServicesDefinition [-Name <String>] -DisplayName <String> -ManagedByTenantId <String>
 [-Description <String>] -Authorization <Authorization[]> -PlanName <String> -PlanPublisher <String>
 -PlanProduct <String> -PlanVersion <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b12fb-107">ByAuthorization</span><span class="sxs-lookup"><span data-stu-id="b12fb-107">ByAuthorization</span></span>
```
New-AzManagedServicesDefinition [-Name <String>] -DisplayName <String> -ManagedByTenantId <String>
 [-Description <String>] -Authorization <Authorization[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b12fb-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b12fb-108">DESCRIPTION</span></span>
<span data-ttu-id="b12fb-109">Создание или обновление определения регистрации.</span><span class="sxs-lookup"><span data-stu-id="b12fb-109">Creates or updates a registration definition.</span></span>

## <span data-ttu-id="b12fb-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b12fb-110">EXAMPLES</span></span>

### <span data-ttu-id="b12fb-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b12fb-111">Example 1</span></span>
```
PS C:\> New-AzManagedServicesDefinition -DisplayName "MyTestDefinition" -ManagedByTenantId 72f9acbf-86f1-41af-91ab-2d7ef011db47 -RoleDefinitionId acdd72a7-3385-48ef-bd42-f606fba81ae7 -PrincipalId 714160ec-87d5-42bb-8b17-287c0dd7417d

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
b732e39c-c034-44cd-b5a1-094669ccc8c5 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/b732e39c-c034-44cd-b5a1-094669ccc8c5 Succeeded


PS C:\>
```

<span data-ttu-id="b12fb-112">Создает определение регистрации по значениям roleDefinitionId и principalId, заданным непосредственно.</span><span class="sxs-lookup"><span data-stu-id="b12fb-112">Creates a registration definition by roleDefinitionId and principalId values given directly.</span></span>

### <span data-ttu-id="b12fb-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="b12fb-113">Example 2</span></span>
```
PS C:\> $auths = @(
>>   [Microsoft.Azure.Management.ManagedServices.Models.Authorization]@{RoleDefinitionId = "acdd72a7-3385-48ef-bd42-f606fba81ae7"; PrincipalId = "714160ec-87d5-42bb-8b17-287c0dd7417d" }
>>  );
PS C:\> $definition = New-AzManagedServicesDefinition -DisplayName "MyTestDefinition" -ManagedByTenantId 72f9acbf-86f1-41af-91ab-2d7ef011db47 -Authorization $auths
PS C:\> $definition

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
55a89269-0347-4a9c-a778-c3f37b9f8672 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/55a89269-0347-4a9c-a778-c3f37b9f8672 Succeeded


PS C:\>
```

<span data-ttu-id="b12fb-114">Создание или обновление определения регистрации с подробными сведениями о авторизации.</span><span class="sxs-lookup"><span data-stu-id="b12fb-114">Creates or updates a registration definition with authorization details.</span></span>

### <span data-ttu-id="b12fb-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="b12fb-115">Example 3</span></span>
```
PS C:\> $auths = @(
>>   [Microsoft.Azure.Management.ManagedServices.Models.Authorization]@{RoleDefinitionId = "acdd72a7-3385-48ef-bd42-f606fba81ae7"; PrincipalId = "714160ec-87d5-42bb-8b17-287c0dd7417d" },
>>   [Microsoft.Azure.Management.ManagedServices.Models.Authorization]@{RoleDefinitionId = "9980e02c-c2be-4d73-94e8-173b1dc7cf3c"; PrincipalId = "714160ec-87d5-42bb-8b17-287c0dd7417d" }
>>  );
PS C:\> $definition = Get-AzManagedServicesDefinition
PS C:\> $definition.Properties.Authorization

PrincipalId                          RoleDefinitionId
-----------                          ----------------
714160ec-87d5-42bb-8b17-287c0dd7417d acdd72a7-3385-48ef-bd42-f606fba81ae7


PS C:\> $definition.Name
55a89269-0347-4a9c-a778-c3f37b9f8672
PS C:\> $definition = New-AzManagedServicesDefinition -DisplayName "MyTestDefinition" -ManagedByTenantId 72f9acbf-86f1-41af-91ab-2d7ef011db47 -Authorization $auths -Name 55a89269-0347-4a9c-a778-c3f37b9f8672
PS C:\> $definition.Properties.Authorization

PrincipalId                          RoleDefinitionId
-----------                          ----------------
714160ec-87d5-42bb-8b17-287c0dd7417d acdd72a7-3385-48ef-bd42-f606fba81ae7
714160ec-87d5-42bb-8b17-287c0dd7417d 9980e02c-c2be-4d73-94e8-173b1dc7cf3c

PS C:\>
```

<span data-ttu-id="b12fb-116">Обновляет определение регистрации с подробными сведениями о авторизации и его именем.</span><span class="sxs-lookup"><span data-stu-id="b12fb-116">Updates a registration definition with authorization details and name of the registration definition.</span></span>

## <span data-ttu-id="b12fb-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b12fb-117">PARAMETERS</span></span>

### <span data-ttu-id="b12fb-118">-Authorization</span><span class="sxs-lookup"><span data-stu-id="b12fb-118">-Authorization</span></span>
<span data-ttu-id="b12fb-119">Список сопоставления авторизации с principalId — roleDefinitionId.</span><span class="sxs-lookup"><span data-stu-id="b12fb-119">The authorization mapping list with principalId - roleDefinitionId.</span></span>

```yaml
Type: Microsoft.Azure.Management.ManagedServices.Models.Authorization[]
Parameter Sets: ByPlan, ByAuthorization
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b12fb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b12fb-120">-DefaultProfile</span></span>
<span data-ttu-id="b12fb-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b12fb-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b12fb-122">-Description</span><span class="sxs-lookup"><span data-stu-id="b12fb-122">-Description</span></span>
<span data-ttu-id="b12fb-123">Описание определения регистрации.</span><span class="sxs-lookup"><span data-stu-id="b12fb-123">The description of the Registration Definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b12fb-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="b12fb-124">-DisplayName</span></span>
<span data-ttu-id="b12fb-125">Отображаемая имя определения регистрации.</span><span class="sxs-lookup"><span data-stu-id="b12fb-125">The display name of the Registration Definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b12fb-126">-ManagedByTenantId</span><span class="sxs-lookup"><span data-stu-id="b12fb-126">-ManagedByTenantId</span></span>
<span data-ttu-id="b12fb-127">Идентификатор клиента ManagedBy.</span><span class="sxs-lookup"><span data-stu-id="b12fb-127">The ManagedBy Tenant Identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b12fb-128">-Name</span><span class="sxs-lookup"><span data-stu-id="b12fb-128">-Name</span></span>
<span data-ttu-id="b12fb-129">Уникальное имя определения регистрации.</span><span class="sxs-lookup"><span data-stu-id="b12fb-129">The unique name of the Registration Definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b12fb-130">-PlanName</span><span class="sxs-lookup"><span data-stu-id="b12fb-130">-PlanName</span></span>
<span data-ttu-id="b12fb-131">Название плана.</span><span class="sxs-lookup"><span data-stu-id="b12fb-131">The name of the plan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPlan
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b12fb-132">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="b12fb-132">-PlanProduct</span></span>
<span data-ttu-id="b12fb-133">Название продукта.</span><span class="sxs-lookup"><span data-stu-id="b12fb-133">The name of the Product.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPlan
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b12fb-134">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="b12fb-134">-PlanPublisher</span></span>
<span data-ttu-id="b12fb-135">Имя издателя.</span><span class="sxs-lookup"><span data-stu-id="b12fb-135">The name of the Publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPlan
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b12fb-136">-PlanVersion</span><span class="sxs-lookup"><span data-stu-id="b12fb-136">-PlanVersion</span></span>
<span data-ttu-id="b12fb-137">Номер версии плана.</span><span class="sxs-lookup"><span data-stu-id="b12fb-137">The version number of the plan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPlan
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b12fb-138">-PrincipalId</span><span class="sxs-lookup"><span data-stu-id="b12fb-138">-PrincipalId</span></span>
<span data-ttu-id="b12fb-139">Идентификатор ManagedBy Principal Identifier.</span><span class="sxs-lookup"><span data-stu-id="b12fb-139">The ManagedBy Principal Identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b12fb-140">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="b12fb-140">-RoleDefinitionId</span></span>
<span data-ttu-id="b12fb-141">Идентификатор определения роли, который позволяет предоставить разрешения для основного идентификатора.</span><span class="sxs-lookup"><span data-stu-id="b12fb-141">The role definition identifier to grant permissions to principal identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b12fb-142">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b12fb-142">-AsJob</span></span>
<span data-ttu-id="b12fb-143">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="b12fb-143">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b12fb-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b12fb-144">-Confirm</span></span>
<span data-ttu-id="b12fb-145">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b12fb-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b12fb-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b12fb-146">-WhatIf</span></span>
<span data-ttu-id="b12fb-147">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b12fb-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b12fb-148">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b12fb-148">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b12fb-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b12fb-149">CommonParameters</span></span>
<span data-ttu-id="b12fb-150">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b12fb-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b12fb-151">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b12fb-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b12fb-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b12fb-152">INPUTS</span></span>

### <span data-ttu-id="b12fb-153">Нет</span><span class="sxs-lookup"><span data-stu-id="b12fb-153">None</span></span>
## <span data-ttu-id="b12fb-154">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b12fb-154">OUTPUTS</span></span>

### <span data-ttu-id="b12fb-155">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="b12fb-155">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span></span>
## <span data-ttu-id="b12fb-156">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b12fb-156">NOTES</span></span>

## <span data-ttu-id="b12fb-157">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b12fb-157">RELATED LINKS</span></span>
