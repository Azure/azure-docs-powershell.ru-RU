---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D602F910-B26F-473D-B5B6-C7BDFB0A14CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-Azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzADServicePrincipal.md
ms.openlocfilehash: cd82db28fbf9902b0dedf9415290d769db3ea231
ms.sourcegitcommit: e680033f216d86cd91a1dfdb8328d32f4c99d21a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/02/2021
ms.locfileid: "99251597"
---
# <span data-ttu-id="0c4a9-101">New-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="0c4a9-101">New-AzADServicePrincipal</span></span>

## <span data-ttu-id="0c4a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c4a9-102">SYNOPSIS</span></span>
<span data-ttu-id="0c4a9-103">Создает новую главную службу Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="0c4a9-103">Creates a new azure active directory service principal.</span></span>

## <span data-ttu-id="0c4a9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0c4a9-104">SYNTAX</span></span>

### <span data-ttu-id="0c4a9-105">SimpleParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0c4a9-105">SimpleParameterSet (Default)</span></span>
```
New-AzADServicePrincipal [-ApplicationId <Guid>] [-DisplayName <String>] [-Password <SecureString>]
 [-StartDate <DateTime>] [-EndDate <DateTime>] [-Scope <String>] [-Role <String>] [-SkipAssignment]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c4a9-106">ApplicationWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c4a9-106">ApplicationWithoutCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c4a9-107">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c4a9-107">ApplicationWithPasswordPlainParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c4a9-108">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c4a9-108">ApplicationWithPasswordCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c4a9-109">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c4a9-109">ApplicationWithKeyPlainParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c4a9-110">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c4a9-110">ApplicationWithKeyCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c4a9-111">DisplayNameWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c4a9-111">DisplayNameWithoutCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c4a9-112">DisplayNameWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c4a9-112">DisplayNameWithPasswordPlainParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c4a9-113">DisplayNameWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c4a9-113">DisplayNameWithPasswordCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c4a9-114">DisplayNameWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c4a9-114">DisplayNameWithKeyPlainParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c4a9-115">DisplayNameWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c4a9-115">DisplayNameWithKeyCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c4a9-116">ApplicationObjectWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c4a9-116">ApplicationObjectWithoutCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c4a9-117">ApplicationObjectWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c4a9-117">ApplicationObjectWithPasswordPlainParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -Password <SecureString>
 [-StartDate <DateTime>] [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0c4a9-118">ApplicationObjectWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c4a9-118">ApplicationObjectWithPasswordCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication>
 -PasswordCredential <PSADPasswordCredential[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0c4a9-119">ApplicationObjectWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c4a9-119">ApplicationObjectWithKeyPlainParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c4a9-120">ApplicationObjectWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c4a9-120">ApplicationObjectWithKeyCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c4a9-121">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0c4a9-121">DESCRIPTION</span></span>
<span data-ttu-id="0c4a9-122">Создает новую главную службу Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="0c4a9-122">Creates a new azure active directory service principal.</span></span> <span data-ttu-id="0c4a9-123">В наборе параметров по умолчанию используются значения по умолчанию для параметров, если пользователь не предоставляет их.</span><span class="sxs-lookup"><span data-stu-id="0c4a9-123">The default parameter set uses default values for parameters if the user does not provide one for them.</span></span> <span data-ttu-id="0c4a9-124">Дополнительные сведения об используемых значениях по умолчанию см. в описании параметров ниже.</span><span class="sxs-lookup"><span data-stu-id="0c4a9-124">For more information on the default values used, please see the description for the given parameters below.</span></span>
<span data-ttu-id="0c4a9-125">Этот cmdlet может назначать роль главе службы с параметрами и их параметрами; если ни один из этих параметров не задан, роль не назначается. `Role` `Scope`</span><span class="sxs-lookup"><span data-stu-id="0c4a9-125">This cmdlet has the ability to assign a role to the service principal with the `Role` and `Scope` parameters; if neither of these parameters are provided, no role will be assigned to the service principal.</span></span> <span data-ttu-id="0c4a9-126">По умолчанию для параметров и параметров заданы "Участник" и текущая подписка соответственно (примечание: значения по умолчанию используются только в том случае, если пользователь предоставляет значение для одного из двух параметров, но не `Role` `Scope` для другого).</span><span class="sxs-lookup"><span data-stu-id="0c4a9-126">The default values for the `Role` and `Scope` parameters are "Contributor" and the current subscription, respectively (_note_: the defaults are only used when the user provides a value for one of the two parameters, but not the other).</span></span>
<span data-ttu-id="0c4a9-127">Он также неявно создает приложение и задает его свойства (если он не предоставлен).</span><span class="sxs-lookup"><span data-stu-id="0c4a9-127">The cmdlet also implicitly creates an application and sets its properties (if the ApplicationId is not provided).</span></span> <span data-ttu-id="0c4a9-128">Для обновления параметров приложения используйте Set-AzADApplication.</span><span class="sxs-lookup"><span data-stu-id="0c4a9-128">In order to update the application specific parameters please use Set-AzADApplication cmdlet.</span></span>

> [!WARNING]
> <span data-ttu-id="0c4a9-129">Когда вы создаете главную службу с помощью команды **New-AzADServicePrincipal,** выходные данные включают учетные данные, которые необходимо защитить.</span><span class="sxs-lookup"><span data-stu-id="0c4a9-129">When you create a service principal using the **New-AzADServicePrincipal** command, the output includes credentials that you must protect.</span></span> <span data-ttu-id="0c4a9-130">В качестве альтернативы можно использовать [управляемые удостоверения,](/azure/active-directory/managed-identities-azure-resources/overview) чтобы избежать необходимости использовать учетные данные.</span><span class="sxs-lookup"><span data-stu-id="0c4a9-130">As an alternative, consider using [managed identities](/azure/active-directory/managed-identities-azure-resources/overview) to avoid the need to use credentials.</span></span>
>
> <span data-ttu-id="0c4a9-131">По умолчанию **New-AzADServicePrincipal** назначает [](/azure/role-based-access-control/built-in-roles#contributor) роль Участника основной службе в области подписки.</span><span class="sxs-lookup"><span data-stu-id="0c4a9-131">By default, **New-AzADServicePrincipal** assigns the [Contributor](/azure/role-based-access-control/built-in-roles#contributor) role to the service principal at the subscription scope.</span></span> <span data-ttu-id="0c4a9-132">Чтобы снизить риск компрометации основной службы, назначьте более определенную роль и сузьте область действия до группы ресурсов или ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0c4a9-132">To reduce your risk of a compromised service principal, assign a more specific role and narrow the scope to a resource or resource group.</span></span> <span data-ttu-id="0c4a9-133">Дополнительные [сведения см. в сведениях](/azure/role-based-access-control/role-assignments-steps) о добавлении назначения роли в этой области.</span><span class="sxs-lookup"><span data-stu-id="0c4a9-133">See [Steps to add a role assignment](/azure/role-based-access-control/role-assignments-steps) for more information.</span></span>

## <span data-ttu-id="0c4a9-134">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0c4a9-134">EXAMPLES</span></span>

### <span data-ttu-id="0c4a9-135">Пример 1. Простое создание основной службы AD</span><span class="sxs-lookup"><span data-stu-id="0c4a9-135">Example 1 - Simple AD service principal creation</span></span>

```
PS C:\> New-AzADServicePrincipal

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal
```

<span data-ttu-id="0c4a9-136">Вышеуказанная команда создает главную службу AD с использованием значений по умолчанию для параметров, которые не предоставлены.</span><span class="sxs-lookup"><span data-stu-id="0c4a9-136">The above command creates an AD service principal using default values for parameters not provided.</span></span> <span data-ttu-id="0c4a9-137">Так как не предоставлены id приложения, для этого деле фигуры службы было создано приложение.</span><span class="sxs-lookup"><span data-stu-id="0c4a9-137">Since an application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="0c4a9-138">Поскольку значения не были за предоставлены или у созданного директора-службы нет `Role` `Scope` разрешений.</span><span class="sxs-lookup"><span data-stu-id="0c4a9-138">Since no values were provided for `Role` or `Scope`, the created service principal does not have any permissions.</span></span>

### <span data-ttu-id="0c4a9-139">Пример 2. Простое создание основной службы AD с заданной ролью и областью по умолчанию</span><span class="sxs-lookup"><span data-stu-id="0c4a9-139">Example 2 - Simple AD service principal creation with a specified role and default scope</span></span>

```
PS C:\> New-AzADServicePrincipal -Role Reader

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal

WARNING: Assigning role 'Reader' over scope '/subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz' to the new service principal.
```

<span data-ttu-id="0c4a9-140">С помощью этой команды создается principal-служба AD, используя значения по умолчанию для параметров, которые не предоставлены.</span><span class="sxs-lookup"><span data-stu-id="0c4a9-140">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="0c4a9-141">Так как не предоставлен id приложения, для основного обслуживания было создано приложение.</span><span class="sxs-lookup"><span data-stu-id="0c4a9-141">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="0c4a9-142">Principal service principal was created with "Reader" permissions over the current subscription (since no value was provided for the `Scope` parameter).</span><span class="sxs-lookup"><span data-stu-id="0c4a9-142">The service principal was created with "Reader" permissions over the current subscription (since no value was provided for the `Scope` parameter).</span></span>

### <span data-ttu-id="0c4a9-143">Пример 3. Простое создание основной службы AD с заданной областью и ролью по умолчанию</span><span class="sxs-lookup"><span data-stu-id="0c4a9-143">Example 3 - Simple AD service principal creation with a specified scope and default role</span></span>

```
PS C:\> New-AzADServicePrincipal -Scope /subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal

WARNING: Assigning role 'Contributor' over scope '/subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup' to the new service principal.
```

<span data-ttu-id="0c4a9-144">С помощью этой команды создается principal-служба AD, используя значения по умолчанию для параметров, которые не предоставлены.</span><span class="sxs-lookup"><span data-stu-id="0c4a9-144">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="0c4a9-145">Так как не предоставлен id приложения, для основного обслуживания было создано приложение.</span><span class="sxs-lookup"><span data-stu-id="0c4a9-145">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="0c4a9-146">Principal service principal was created with "Contributor" permissions (since no value was provided for the `Role` parameter) over the provided resource group scope.</span><span class="sxs-lookup"><span data-stu-id="0c4a9-146">The service principal was created with "Contributor" permissions (since no value was provided for the `Role` parameter) over the provided resource group scope.</span></span>

### <span data-ttu-id="0c4a9-147">Пример 4. Простое создание основной службы AD с заданной областью и ролью</span><span class="sxs-lookup"><span data-stu-id="0c4a9-147">Example 4 - Simple AD service principal creation with a specified scope and role</span></span>

```
PS C:\> New-AzADServicePrincipal -Role Reader -Scope /subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal

WARNING: Assigning role 'Reader' over scope '/subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup' to the new service principal.
```

<span data-ttu-id="0c4a9-148">С помощью этой команды создается principal-служба AD, используя значения по умолчанию для параметров, которые не предоставлены.</span><span class="sxs-lookup"><span data-stu-id="0c4a9-148">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="0c4a9-149">Так как не предоставлен id приложения, для основного обслуживания было создано приложение.</span><span class="sxs-lookup"><span data-stu-id="0c4a9-149">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="0c4a9-150">Проект-служба была создана с разрешениями "Читатель" для за предоставленной области действия группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0c4a9-150">The service principal was created with "Reader" permissions over the provided resource group scope.</span></span>

### <span data-ttu-id="0c4a9-151">Пример 5. Создание новой основной роли службы AD с использованием ид приложения с назначением роли</span><span class="sxs-lookup"><span data-stu-id="0c4a9-151">Example 5 - Create a new AD service principal using application id with role assignment</span></span>

```
PS C:\> New-AzADServicePrincipal -ApplicationId 34a28ad2-dec4-4a41-bc3b-d22ddf90000e

ServicePrincipalNames : {34a28ad2-dec4-4a41-bc3b-d22ddf90000e, http://my-temp-app}
ApplicationId         : 34a28ad2-dec4-4a41-bc3b-d22ddf90000e
DisplayName           : my-temp-app
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal
```

<span data-ttu-id="0c4a9-152">Создает для приложения новую главную службу AD с ид приложения 34a28ad2-dec4-4a41-bc3b-d22ddf90000e.</span><span class="sxs-lookup"><span data-stu-id="0c4a9-152">Creates a new AD service principal for the application with application id '34a28ad2-dec4-4a41-bc3b-d22ddf90000e'.</span></span> <span data-ttu-id="0c4a9-153">Поскольку значения не были за предоставлены или у созданного директора-службы нет `Role` `Scope` разрешений.</span><span class="sxs-lookup"><span data-stu-id="0c4a9-153">Since no values were provided for `Role` or `Scope`, the created service principal does not have any permissions.</span></span>

### <span data-ttu-id="0c4a9-154">Пример 6. Создание новой основной суммы службы AD с помощью piping</span><span class="sxs-lookup"><span data-stu-id="0c4a9-154">Example 6 - Create a new AD service principal using piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId 3ede3c26-b443-4e0b-9efc-b05e68338dc3 | New-AzADServicePrincipal
```

<span data-ttu-id="0c4a9-155">Получает приложение с объектным ид '3ede3c26-b443-4e0b-9efc-b05e68338dc3' и трубами к New-AzADServicePrincipal- и создает для этого приложения новую главную службу AD.</span><span class="sxs-lookup"><span data-stu-id="0c4a9-155">Gets the application with object id '3ede3c26-b443-4e0b-9efc-b05e68338dc3' and pipes that to the New-AzADServicePrincipal cmdlet to create a new AD service principal for that application.</span></span>

## <span data-ttu-id="0c4a9-156">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0c4a9-156">PARAMETERS</span></span>

### <span data-ttu-id="0c4a9-157">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="0c4a9-157">-ApplicationId</span></span>
<span data-ttu-id="0c4a9-158">Уникальный ид приложения для основной службы в клиенте.</span><span class="sxs-lookup"><span data-stu-id="0c4a9-158">The unique application id for a service principal in a tenant.</span></span>
<span data-ttu-id="0c4a9-159">Созданное свойство невозможно изменить.</span><span class="sxs-lookup"><span data-stu-id="0c4a9-159">Once created this property cannot be changed.</span></span>
<span data-ttu-id="0c4a9-160">Если не указан ид приложения, он будет создан.</span><span class="sxs-lookup"><span data-stu-id="0c4a9-160">If an application id is not specified, one will be generated.</span></span>

```yaml
Type: System.Guid
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Guid
Parameter Sets: ApplicationWithoutCredentialParameterSet, ApplicationWithPasswordPlainParameterSet, ApplicationWithPasswordCredentialParameterSet, ApplicationWithKeyPlainParameterSet, ApplicationWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c4a9-161">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="0c4a9-161">-ApplicationObject</span></span>
<span data-ttu-id="0c4a9-162">Объект, представляющий приложение, для которого создается principal-служба.</span><span class="sxs-lookup"><span data-stu-id="0c4a9-162">The object representing the application for which the service principal is created.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectWithoutCredentialParameterSet, ApplicationObjectWithPasswordPlainParameterSet, ApplicationObjectWithPasswordCredentialParameterSet, ApplicationObjectWithKeyPlainParameterSet, ApplicationObjectWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0c4a9-163">-CertValue</span><span class="sxs-lookup"><span data-stu-id="0c4a9-163">-CertValue</span></span>
<span data-ttu-id="0c4a9-164">Значение асимметричного типа учетных данных.</span><span class="sxs-lookup"><span data-stu-id="0c4a9-164">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="0c4a9-165">Он представляет собой 64-кодированный сертификат.</span><span class="sxs-lookup"><span data-stu-id="0c4a9-165">It represents the base 64 encoded certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationWithKeyPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ApplicationObjectWithKeyPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c4a9-166">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c4a9-166">-DefaultProfile</span></span>
<span data-ttu-id="0c4a9-167">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="0c4a9-167">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c4a9-168">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="0c4a9-168">-DisplayName</span></span>
<span data-ttu-id="0c4a9-169">Удобное имя директора-службы.</span><span class="sxs-lookup"><span data-stu-id="0c4a9-169">The friendly name of the service principal.</span></span> <span data-ttu-id="0c4a9-170">Если отображаемого имени нет, по умолчанию для этого значения будет зафикс "azure-powershell-MM-dd-y-HH-mm-ss", где суффикс — время создания приложения.</span><span class="sxs-lookup"><span data-stu-id="0c4a9-170">If a display name is not provided, this value will default to 'azure-powershell-MM-dd-yyyy-HH-mm-ss', where the suffix is the time of application creation.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DisplayNameWithoutCredentialParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithPasswordCredentialParameterSet, DisplayNameWithKeyPlainParameterSet, DisplayNameWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c4a9-171">-EndDate</span><span class="sxs-lookup"><span data-stu-id="0c4a9-171">-EndDate</span></span>
<span data-ttu-id="0c4a9-172">Дата окончания использования учетных данных.</span><span class="sxs-lookup"><span data-stu-id="0c4a9-172">The effective end date of the credential usage.</span></span>
<span data-ttu-id="0c4a9-173">Значение даты окончания по умолчанию составляет один год от сегодняшнего дня.</span><span class="sxs-lookup"><span data-stu-id="0c4a9-173">The default end date value is one year from today.</span></span> <span data-ttu-id="0c4a9-174">Для учетных данных асимметричного типа необходимо установить этот учетный данные в день, когда допустим сертификат X509, или до нее.</span><span class="sxs-lookup"><span data-stu-id="0c4a9-174">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: SimpleParameterSet, ApplicationObjectWithPasswordPlainParameterSet, ApplicationObjectWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c4a9-175">-KeyCredential</span><span class="sxs-lookup"><span data-stu-id="0c4a9-175">-KeyCredential</span></span>
<span data-ttu-id="0c4a9-176">Набор учетных данных ключа, связанных с приложением.</span><span class="sxs-lookup"><span data-stu-id="0c4a9-176">The collection of key credentials associated with the application.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADKeyCredential[]
Parameter Sets: ApplicationWithKeyCredentialParameterSet, DisplayNameWithKeyCredentialParameterSet
Aliases: KeyCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADKeyCredential[]
Parameter Sets: ApplicationObjectWithKeyCredentialParameterSet
Aliases: KeyCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c4a9-177">-Password</span><span class="sxs-lookup"><span data-stu-id="0c4a9-177">-Password</span></span>
<span data-ttu-id="0c4a9-178">Пароль, который должен быть связан с главой службы.</span><span class="sxs-lookup"><span data-stu-id="0c4a9-178">The password to be associated with the service principal.</span></span> <span data-ttu-id="0c4a9-179">Если пароль не задан, в качестве пароля создается случайный GUID.</span><span class="sxs-lookup"><span data-stu-id="0c4a9-179">If a password is not provided, a random GUID will be generated and used as the password.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Security.SecureString
Parameter Sets: ApplicationWithPasswordPlainParameterSet, DisplayNameWithPasswordPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Security.SecureString
Parameter Sets: ApplicationObjectWithPasswordPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c4a9-180">-PasswordCredential</span><span class="sxs-lookup"><span data-stu-id="0c4a9-180">-PasswordCredential</span></span>
<span data-ttu-id="0c4a9-181">Набор учетных данных, связанных с приложением.</span><span class="sxs-lookup"><span data-stu-id="0c4a9-181">The collection of password credentials associated with the application.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADPasswordCredential[]
Parameter Sets: ApplicationWithPasswordCredentialParameterSet, DisplayNameWithPasswordCredentialParameterSet
Aliases: PasswordCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADPasswordCredential[]
Parameter Sets: ApplicationObjectWithPasswordCredentialParameterSet
Aliases: PasswordCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c4a9-182">-Роль</span><span class="sxs-lookup"><span data-stu-id="0c4a9-182">-Role</span></span>
<span data-ttu-id="0c4a9-183">Роль, которая является основной службой в рамках этой области.</span><span class="sxs-lookup"><span data-stu-id="0c4a9-183">The role that the service principal has over the scope.</span></span> <span data-ttu-id="0c4a9-184">Если для нее есть значение, но для нее не за предоставлено значение, по умолчанию будет засве же `Scope` `Role` роль `Role` "Участник".</span><span class="sxs-lookup"><span data-stu-id="0c4a9-184">If a value for `Scope` is provided, but no value is provided for `Role`, then `Role` will default to the 'Contributor' role.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c4a9-185">-Scope</span><span class="sxs-lookup"><span data-stu-id="0c4a9-185">-Scope</span></span>
<span data-ttu-id="0c4a9-186">Область, для которую у директора-службы есть разрешения.</span><span class="sxs-lookup"><span data-stu-id="0c4a9-186">The scope that the service principal has permissions on.</span></span> <span data-ttu-id="0c4a9-187">Если значение за предоставлено, но для нее не за предоставлено значение, по умолчанию будет активна `Role` `Scope` `Scope` текущая подписка.</span><span class="sxs-lookup"><span data-stu-id="0c4a9-187">If a value for `Role` is provided, but no value is provided for `Scope`, then `Scope` will default to the current subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c4a9-188">-SkipAssignment</span><span class="sxs-lookup"><span data-stu-id="0c4a9-188">-SkipAssignment</span></span>
<span data-ttu-id="0c4a9-189">Если за установлено, будет пропущено создание назначения роли по умолчанию для основного задания службы.</span><span class="sxs-lookup"><span data-stu-id="0c4a9-189">If set, will skip creating the default role assignment for the service principal.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c4a9-190">-StartDate</span><span class="sxs-lookup"><span data-stu-id="0c4a9-190">-StartDate</span></span>
<span data-ttu-id="0c4a9-191">Начальную дату использования учетных данных.</span><span class="sxs-lookup"><span data-stu-id="0c4a9-191">The effective start date of the credential usage.</span></span>
<span data-ttu-id="0c4a9-192">По умолчанию дата начала является сегодняшним значением.</span><span class="sxs-lookup"><span data-stu-id="0c4a9-192">The default start date value is today.</span></span> <span data-ttu-id="0c4a9-193">Для "асимметричных" учетных данных этого типа необходимо установить в день, начиная с даты действия сертификата X509, или после нее.</span><span class="sxs-lookup"><span data-stu-id="0c4a9-193">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: SimpleParameterSet, ApplicationObjectWithPasswordPlainParameterSet, ApplicationObjectWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c4a9-194">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0c4a9-194">-Confirm</span></span>
<span data-ttu-id="0c4a9-195">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="0c4a9-195">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c4a9-196">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c4a9-196">-WhatIf</span></span>
<span data-ttu-id="0c4a9-197">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c4a9-197">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c4a9-198">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="0c4a9-198">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c4a9-199">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c4a9-199">CommonParameters</span></span>
<span data-ttu-id="0c4a9-200">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c4a9-200">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c4a9-201">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c4a9-201">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c4a9-202">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0c4a9-202">INPUTS</span></span>

### <span data-ttu-id="0c4a9-203">System.Guid</span><span class="sxs-lookup"><span data-stu-id="0c4a9-203">System.Guid</span></span>

### <span data-ttu-id="0c4a9-204">System.String</span><span class="sxs-lookup"><span data-stu-id="0c4a9-204">System.String</span></span>

### <span data-ttu-id="0c4a9-205">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="0c4a9-205">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="0c4a9-206">Параметры: ApplicationObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0c4a9-206">Parameters: ApplicationObject (ByValue)</span></span>

### <span data-ttu-id="0c4a9-207">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADPasswordCredential[]</span><span class="sxs-lookup"><span data-stu-id="0c4a9-207">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADPasswordCredential[]</span></span>

### <span data-ttu-id="0c4a9-208">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADKeyCredential[]</span><span class="sxs-lookup"><span data-stu-id="0c4a9-208">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADKeyCredential[]</span></span>

### <span data-ttu-id="0c4a9-209">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="0c4a9-209">System.Security.SecureString</span></span>

### <span data-ttu-id="0c4a9-210">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="0c4a9-210">System.DateTime</span></span>

## <span data-ttu-id="0c4a9-211">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0c4a9-211">OUTPUTS</span></span>

### <span data-ttu-id="0c4a9-212">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="0c4a9-212">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="0c4a9-213">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADServicePrincipalWrapper</span><span class="sxs-lookup"><span data-stu-id="0c4a9-213">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADServicePrincipalWrapper</span></span>

## <span data-ttu-id="0c4a9-214">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0c4a9-214">NOTES</span></span>
<span data-ttu-id="0c4a9-215">Ключевые слова: azure, Az, arm, resource, management, manager, resource, group, template, deployment</span><span class="sxs-lookup"><span data-stu-id="0c4a9-215">Keywords: azure, Az, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="0c4a9-216">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0c4a9-216">RELATED LINKS</span></span>

[<span data-ttu-id="0c4a9-217">Remove-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="0c4a9-217">Remove-AzADServicePrincipal</span></span>](./Remove-AzADServicePrincipal.md)

[<span data-ttu-id="0c4a9-218">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="0c4a9-218">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

[<span data-ttu-id="0c4a9-219">New-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="0c4a9-219">New-AzADApplication</span></span>](./New-AzADApplication.md)

[<span data-ttu-id="0c4a9-220">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="0c4a9-220">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="0c4a9-221">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="0c4a9-221">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

[<span data-ttu-id="0c4a9-222">New-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="0c4a9-222">New-AzADSpCredential</span></span>](./New-AzADSpCredential.md)

[<span data-ttu-id="0c4a9-223">Remove-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="0c4a9-223">Remove-AzADSpCredential</span></span>](./Remove-AzADSpCredential.md)

