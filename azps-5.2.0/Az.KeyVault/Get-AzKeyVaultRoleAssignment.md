---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultRoleAssignment.md
ms.openlocfilehash: c610339bf90069f30d6107d46fc92fd896d6816c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98323906"
---
# <span data-ttu-id="61169-101">Get-AzKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="61169-101">Get-AzKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="61169-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61169-102">SYNOPSIS</span></span>
<span data-ttu-id="61169-103">Получить или перечислить назначения ролей для управляемой HSM.</span><span class="sxs-lookup"><span data-stu-id="61169-103">Get or list role assignments of a managed HSM.</span></span> <span data-ttu-id="61169-104">Используйте соответствующие параметры для списка назначений определенному пользователю или определению роли.</span><span class="sxs-lookup"><span data-stu-id="61169-104">Use respective parameters to list assignments to a specific user or a role definition.</span></span>

## <span data-ttu-id="61169-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="61169-105">SYNTAX</span></span>

### <span data-ttu-id="61169-106">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="61169-106">List (Default)</span></span>
```
Get-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] [-RoleDefinitionName <String>]
 [-RoleDefinitionId <String>] [-ObjectId <String>] [-SignInName <String>] [-ApplicationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="61169-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="61169-107">GetByName</span></span>
```
Get-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleAssignmentName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="61169-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="61169-108">DESCRIPTION</span></span>
<span data-ttu-id="61169-109">Используйте эту `Get-AzKeyVaultRoleAssignment` команду для списка всех назначений ролей, которые эффективны по области.</span><span class="sxs-lookup"><span data-stu-id="61169-109">Use the `Get-AzKeyVaultRoleAssignment` command to list all role assignments that are effective on a scope.</span></span>
<span data-ttu-id="61169-110">Эта команда возвращает все назначения ролей, присвоенные управляемой функции управления HSM без параметров.</span><span class="sxs-lookup"><span data-stu-id="61169-110">Without any parameters, this command returns all the role assignments made under the managed HSM.</span></span>
<span data-ttu-id="61169-111">Этот список можно отфильтровать с помощью параметров фильтрации для основных ролей и областей.</span><span class="sxs-lookup"><span data-stu-id="61169-111">This list can be filtered using filtering parameters for principal, role and scope.</span></span>
<span data-ttu-id="61169-112">Необходимо у указывается тема задания.</span><span class="sxs-lookup"><span data-stu-id="61169-112">The subject of the assignment must be specified.</span></span>
<span data-ttu-id="61169-113">Чтобы указать пользователя, используйте параметры SignInName или Azure AD ObjectId.</span><span class="sxs-lookup"><span data-stu-id="61169-113">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="61169-114">Чтобы указать группу безопасности, используйте параметр Azure AD ObjectId.</span><span class="sxs-lookup"><span data-stu-id="61169-114">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="61169-115">Чтобы указать приложение Azure AD, используйте параметры ApplicationId или ObjectId.</span><span class="sxs-lookup"><span data-stu-id="61169-115">And to specify an Azure AD application, use ApplicationId or ObjectId parameters.</span></span>
<span data-ttu-id="61169-116">Роль, которая должна быть назначена, должна быть указана с помощью параметра RoleDefinitionName или RoleDefinitionId.</span><span class="sxs-lookup"><span data-stu-id="61169-116">The role that is being assigned must be specified using the RoleDefinitionName or RoleDefinitionId parameter.</span></span>
<span data-ttu-id="61169-117">Может быть указана область, для которой предоставляется доступ.</span><span class="sxs-lookup"><span data-stu-id="61169-117">The scope at which access is being granted may be specified.</span></span> <span data-ttu-id="61169-118">Значение по умолчанию — "/".</span><span class="sxs-lookup"><span data-stu-id="61169-118">It defaults to "/".</span></span>

## <span data-ttu-id="61169-119">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="61169-119">EXAMPLES</span></span>

### <span data-ttu-id="61169-120">Пример 1</span><span class="sxs-lookup"><span data-stu-id="61169-120">Example 1</span></span>
```powershell
PS C:\> Get-AzKeyVaultRoleAssignment -HsmName myHsm

RoleDefinitionName         DisplayName                      ObjectType Scope
------------------         -----------                      ---------- -----
Managed HSM Administrator  User 1 (user1@microsoft.com)     User       /
Managed HSM Crypto Auditor User 2 (user2@microsoft.com)     User       /keys
Managed HSM Backup         User 2 (user2@microsoft.com)     User       /
Managed HSM Administrator  User 2 (user2@microsoft.com)     User       /
```

<span data-ttu-id="61169-121">В этом примере перечислены все назначения ролей myHsm по всей области.</span><span class="sxs-lookup"><span data-stu-id="61169-121">This example lists all role assignments of "myHsm" on all the scope.</span></span>

### <span data-ttu-id="61169-122">Пример 2</span><span class="sxs-lookup"><span data-stu-id="61169-122">Example 2</span></span>
```powershell
PS C:\> Get-AzKeyVaultRoleAssignment -HsmName myHsm -SignInName user1@microsoft.com -Scope "/keys"

RoleDefinitionName         DisplayName                      ObjectType Scope
------------------         -----------                      ---------- -----
Managed HSM Crypto Auditor User 1 (user1@microsoft.com)     User       /keys
Managed HSM Backup         User 1 (user1@microsoft.com)     User       /keys
```

<span data-ttu-id="61169-123">В этом примере перечислены все назначения ролей "myHsm" в области "/keys" и результаты фильтруются по имени пользователя для регистрации.</span><span class="sxs-lookup"><span data-stu-id="61169-123">This example lists all role assignments of "myHsm" on "/keys" scope and filters the result by user sign-in name.</span></span>

## <span data-ttu-id="61169-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="61169-124">PARAMETERS</span></span>

### <span data-ttu-id="61169-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="61169-125">-ApplicationId</span></span>
<span data-ttu-id="61169-126">SpN приложения.</span><span class="sxs-lookup"><span data-stu-id="61169-126">The app SPN.</span></span>

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

### <span data-ttu-id="61169-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61169-127">-DefaultProfile</span></span>
<span data-ttu-id="61169-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="61169-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61169-129">-HsmName</span><span class="sxs-lookup"><span data-stu-id="61169-129">-HsmName</span></span>
<span data-ttu-id="61169-130">Имя HSM.</span><span class="sxs-lookup"><span data-stu-id="61169-130">Name of the HSM.</span></span>

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

### <span data-ttu-id="61169-131">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="61169-131">-ObjectId</span></span>
<span data-ttu-id="61169-132">ИД объекта пользователя или группы.</span><span class="sxs-lookup"><span data-stu-id="61169-132">The user or group object id.</span></span>

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

### <span data-ttu-id="61169-133">-RoleAssignmentName</span><span class="sxs-lookup"><span data-stu-id="61169-133">-RoleAssignmentName</span></span>
<span data-ttu-id="61169-134">Имя назначения роли.</span><span class="sxs-lookup"><span data-stu-id="61169-134">Name of the role assignment.</span></span>

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

### <span data-ttu-id="61169-135">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="61169-135">-RoleDefinitionId</span></span>
<span data-ttu-id="61169-136">ИД роли, назначенной основной роли.</span><span class="sxs-lookup"><span data-stu-id="61169-136">Role Id the principal is assigned to.</span></span>

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

### <span data-ttu-id="61169-137">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="61169-137">-RoleDefinitionName</span></span>
<span data-ttu-id="61169-138">Имя роли, с помощью которого можно назначить главную функцию.</span><span class="sxs-lookup"><span data-stu-id="61169-138">Name of the RBAC role to assign the principal with.</span></span>

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

### <span data-ttu-id="61169-139">-Scope</span><span class="sxs-lookup"><span data-stu-id="61169-139">-Scope</span></span>
<span data-ttu-id="61169-140">Область применения назначения роли или определения, например "/", "/" или "/keys" или "/keys/{keyName}".</span><span class="sxs-lookup"><span data-stu-id="61169-140">Scope at which the role assignment or definition applies to, e.g., '/' or '/keys' or '/keys/{keyName}'.</span></span>
<span data-ttu-id="61169-141">"/" используется в опущении.</span><span class="sxs-lookup"><span data-stu-id="61169-141">'/' is used when omitted.</span></span>

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

### <span data-ttu-id="61169-142">-SignInName</span><span class="sxs-lookup"><span data-stu-id="61169-142">-SignInName</span></span>
<span data-ttu-id="61169-143">Пользователь SignInName.</span><span class="sxs-lookup"><span data-stu-id="61169-143">The user SignInName.</span></span>

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

### <span data-ttu-id="61169-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61169-144">CommonParameters</span></span>
<span data-ttu-id="61169-145">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61169-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61169-146">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="61169-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61169-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="61169-147">INPUTS</span></span>

### <span data-ttu-id="61169-148">Нет</span><span class="sxs-lookup"><span data-stu-id="61169-148">None</span></span>

## <span data-ttu-id="61169-149">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="61169-149">OUTPUTS</span></span>

### <span data-ttu-id="61169-150">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="61169-150">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="61169-151">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="61169-151">NOTES</span></span>

## <span data-ttu-id="61169-152">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="61169-152">RELATED LINKS</span></span>
