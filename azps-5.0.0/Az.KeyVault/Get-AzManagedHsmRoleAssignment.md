---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azmanagedhsmroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzManagedHsmRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzManagedHsmRoleAssignment.md
ms.openlocfilehash: 20e80617d47cd0a1f0ffb5cdb80d836656cd9abd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245306"
---
# <span data-ttu-id="82b31-101">Get-AzManagedHsmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="82b31-101">Get-AzManagedHsmRoleAssignment</span></span>

## <span data-ttu-id="82b31-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="82b31-102">SYNOPSIS</span></span>
<span data-ttu-id="82b31-103">Получение или перечисление назначения ролей управляемого HSM-файла.</span><span class="sxs-lookup"><span data-stu-id="82b31-103">Get or list role assignments of a managed HSM.</span></span> <span data-ttu-id="82b31-104">Используйте соответствующие параметры для присвоения списка назначений определенному пользователю или определению роли.</span><span class="sxs-lookup"><span data-stu-id="82b31-104">Use respective parameters to list assignments to a specific user or a role definition.</span></span>

## <span data-ttu-id="82b31-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="82b31-105">SYNTAX</span></span>

### <span data-ttu-id="82b31-106">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="82b31-106">List (Default)</span></span>
```
Get-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] [-RoleDefinitionName <String>]
 [-RoleDefinitionId <String>] [-ObjectId <String>] [-SignInName <String>] [-ApplicationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="82b31-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="82b31-107">GetByName</span></span>
```
Get-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleAssignmentName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82b31-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="82b31-108">DESCRIPTION</span></span>
<span data-ttu-id="82b31-109">С помощью `Get-AzManagedHsmRoleAssignment` команды можно вывести список всех назначений ролей, действующих в области.</span><span class="sxs-lookup"><span data-stu-id="82b31-109">Use the `Get-AzManagedHsmRoleAssignment` command to list all role assignments that are effective on a scope.</span></span>
<span data-ttu-id="82b31-110">При отсутствии каких бы то ни было параметров эта команда возвращает все назначения ролей, выполненные в управляемом HSM.</span><span class="sxs-lookup"><span data-stu-id="82b31-110">Without any parameters, this command returns all the role assignments made under the managed HSM.</span></span>
<span data-ttu-id="82b31-111">Этот список можно фильтровать с помощью параметров фильтрации для участника, роли и области.</span><span class="sxs-lookup"><span data-stu-id="82b31-111">This list can be filtered using filtering parameters for principal, role and scope.</span></span>
<span data-ttu-id="82b31-112">Необходимо указать тему назначения.</span><span class="sxs-lookup"><span data-stu-id="82b31-112">The subject of the assignment must be specified.</span></span>
<span data-ttu-id="82b31-113">Чтобы указать пользователя, используйте параметры SignInName или Azure AD ObjectId.</span><span class="sxs-lookup"><span data-stu-id="82b31-113">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="82b31-114">Чтобы указать группу безопасности, используйте параметр Azure AD ObjectId.</span><span class="sxs-lookup"><span data-stu-id="82b31-114">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="82b31-115">Чтобы указать приложение Azure AD, используйте параметры ApplicationId или ObjectId.</span><span class="sxs-lookup"><span data-stu-id="82b31-115">And to specify an Azure AD application, use ApplicationId or ObjectId parameters.</span></span>
<span data-ttu-id="82b31-116">Назначаемая роль должна быть указана с помощью параметра RoleDefinitionName или RoleDefinitionId.</span><span class="sxs-lookup"><span data-stu-id="82b31-116">The role that is being assigned must be specified using the RoleDefinitionName or RoleDefinitionId parameter.</span></span>
<span data-ttu-id="82b31-117">Может быть указана область, для которой предоставляется доступ.</span><span class="sxs-lookup"><span data-stu-id="82b31-117">The scope at which access is being granted may be specified.</span></span> <span data-ttu-id="82b31-118">По умолчанию используется значение "/".</span><span class="sxs-lookup"><span data-stu-id="82b31-118">It defaults to "/".</span></span>

## <span data-ttu-id="82b31-119">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="82b31-119">EXAMPLES</span></span>

### <span data-ttu-id="82b31-120">Пример 1</span><span class="sxs-lookup"><span data-stu-id="82b31-120">Example 1</span></span>
```powershell
PS C:\> Get-AzManagedHsmRoleAssignment -HsmName myHsm

RoleDefinitionName         DisplayName                      ObjectType Scope
------------------         -----------                      ---------- -----
Managed HSM Administrator  User 1 (user1@microsoft.com)     User       /
Managed HSM Crypto Auditor User 2 (user2@microsoft.com)     User       /keys
Managed HSM Backup         User 2 (user2@microsoft.com)     User       /
Managed HSM Administrator  User 2 (user2@microsoft.com)     User       /
```

<span data-ttu-id="82b31-121">В этом примере перечислены все назначения ролей "myHsm" для всех областей.</span><span class="sxs-lookup"><span data-stu-id="82b31-121">This example lists all role assignments of "myHsm" on all the scope.</span></span>

### <span data-ttu-id="82b31-122">Пример 2</span><span class="sxs-lookup"><span data-stu-id="82b31-122">Example 2</span></span>
```powershell
PS C:\> Get-AzManagedHsmRoleAssignment -HsmName myHsm -SignInName user1@microsoft.com -Scope "/keys"

RoleDefinitionName         DisplayName                      ObjectType Scope
------------------         -----------                      ---------- -----
Managed HSM Crypto Auditor User 1 (user1@microsoft.com)     User       /keys
Managed HSM Backup         User 1 (user1@microsoft.com)     User       /keys
```

<span data-ttu-id="82b31-123">В этом примере выводятся все назначения ролей "myHsm" в области "/Keys" и фильтруются результаты по имени для входа пользователя.</span><span class="sxs-lookup"><span data-stu-id="82b31-123">This example lists all role assignments of "myHsm" on "/keys" scope and filters the result by user sign-in name.</span></span>

## <span data-ttu-id="82b31-124">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="82b31-124">PARAMETERS</span></span>

### <span data-ttu-id="82b31-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="82b31-125">-ApplicationId</span></span>
<span data-ttu-id="82b31-126">Имя субъекта-службы приложения.</span><span class="sxs-lookup"><span data-stu-id="82b31-126">The app SPN.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases: SPN, ServicePrincipalName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82b31-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82b31-127">-DefaultProfile</span></span>
<span data-ttu-id="82b31-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="82b31-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82b31-129">-HsmName</span><span class="sxs-lookup"><span data-stu-id="82b31-129">-HsmName</span></span>
<span data-ttu-id="82b31-130">Имя HSM.</span><span class="sxs-lookup"><span data-stu-id="82b31-130">Name of the HSM.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82b31-131">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="82b31-131">-ObjectId</span></span>
<span data-ttu-id="82b31-132">Идентификатор объекта пользователя или группы.</span><span class="sxs-lookup"><span data-stu-id="82b31-132">The user or group object id.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases: Id, PrincipalId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82b31-133">-RoleAssignmentName</span><span class="sxs-lookup"><span data-stu-id="82b31-133">-RoleAssignmentName</span></span>
<span data-ttu-id="82b31-134">Имя назначения роли.</span><span class="sxs-lookup"><span data-stu-id="82b31-134">Name of the role assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82b31-135">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="82b31-135">-RoleDefinitionId</span></span>
<span data-ttu-id="82b31-136">Идентификатор роли, которой назначен участник.</span><span class="sxs-lookup"><span data-stu-id="82b31-136">Role Id the principal is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases: RoleId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82b31-137">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="82b31-137">-RoleDefinitionName</span></span>
<span data-ttu-id="82b31-138">Имя роли RBAC, с которой нужно назначить участника.</span><span class="sxs-lookup"><span data-stu-id="82b31-138">Name of the RBAC role to assign the principal with.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases: RoleName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82b31-139">-Scope</span><span class="sxs-lookup"><span data-stu-id="82b31-139">-Scope</span></span>
<span data-ttu-id="82b31-140">Область, к которой относится назначение роли или определение (например, "/" или "/Keys" или "/keys/{keyName}").</span><span class="sxs-lookup"><span data-stu-id="82b31-140">Scope at which the role assignment or definition applies to, e.g., '/' or '/keys' or '/keys/{keyName}'.</span></span>
<span data-ttu-id="82b31-141">"/" используется, если опущен.</span><span class="sxs-lookup"><span data-stu-id="82b31-141">'/' is used when omitted.</span></span>

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

### <span data-ttu-id="82b31-142">-SignInName</span><span class="sxs-lookup"><span data-stu-id="82b31-142">-SignInName</span></span>
<span data-ttu-id="82b31-143">SignInName пользователя.</span><span class="sxs-lookup"><span data-stu-id="82b31-143">The user SignInName.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases: Email, UserPrincipalName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82b31-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82b31-144">CommonParameters</span></span>
<span data-ttu-id="82b31-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="82b31-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82b31-146">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="82b31-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82b31-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="82b31-147">INPUTS</span></span>

### <span data-ttu-id="82b31-148">Ничего</span><span class="sxs-lookup"><span data-stu-id="82b31-148">None</span></span>

## <span data-ttu-id="82b31-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="82b31-149">OUTPUTS</span></span>

### <span data-ttu-id="82b31-150">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="82b31-150">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="82b31-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="82b31-151">NOTES</span></span>

## <span data-ttu-id="82b31-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="82b31-152">RELATED LINKS</span></span>
