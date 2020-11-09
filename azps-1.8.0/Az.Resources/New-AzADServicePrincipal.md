---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D602F910-B26F-473D-B5B6-C7BDFB0A14CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
ms.openlocfilehash: 9db3e3d0fcb52869a53b4bd2b76603d2935c4dd0
ms.sourcegitcommit: 375232b84336ef5e13052504deaa43f5bd4b7f65
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/05/2020
ms.locfileid: "93742970"
---
# <span data-ttu-id="5d3e5-101">New-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="5d3e5-101">New-AzADServicePrincipal</span></span>

## <span data-ttu-id="5d3e5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5d3e5-102">SYNOPSIS</span></span>
<span data-ttu-id="5d3e5-103">Создание нового субъекта-службы Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="5d3e5-103">Creates a new azure active directory service principal.</span></span>

## <span data-ttu-id="5d3e5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5d3e5-104">SYNTAX</span></span>

### <span data-ttu-id="5d3e5-105">SimpleParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5d3e5-105">SimpleParameterSet (Default)</span></span>
```
New-AzADServicePrincipal [-ApplicationId <Guid>] [-DisplayName <String>] [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-Scope <String>] [-Role <String>] [-SkipAssignment]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d3e5-106">ApplicationWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d3e5-106">ApplicationWithoutCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5d3e5-107">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d3e5-107">ApplicationWithPasswordPlainParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d3e5-108">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d3e5-108">ApplicationWithPasswordCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d3e5-109">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d3e5-109">ApplicationWithKeyPlainParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d3e5-110">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d3e5-110">ApplicationWithKeyCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d3e5-111">DisplayNameWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d3e5-111">DisplayNameWithoutCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5d3e5-112">DisplayNameWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d3e5-112">DisplayNameWithPasswordPlainParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d3e5-113">DisplayNameWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d3e5-113">DisplayNameWithPasswordCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d3e5-114">DisplayNameWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d3e5-114">DisplayNameWithKeyPlainParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d3e5-115">DisplayNameWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d3e5-115">DisplayNameWithKeyCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d3e5-116">ApplicationObjectWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d3e5-116">ApplicationObjectWithoutCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d3e5-117">ApplicationObjectWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d3e5-117">ApplicationObjectWithPasswordPlainParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d3e5-118">ApplicationObjectWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d3e5-118">ApplicationObjectWithPasswordCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d3e5-119">ApplicationObjectWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d3e5-119">ApplicationObjectWithKeyPlainParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d3e5-120">ApplicationObjectWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d3e5-120">ApplicationObjectWithKeyCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d3e5-121">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5d3e5-121">DESCRIPTION</span></span>
<span data-ttu-id="5d3e5-122">Создание нового субъекта-службы Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="5d3e5-122">Creates a new azure active directory service principal.</span></span> <span data-ttu-id="5d3e5-123">Параметр по умолчанию использует значения по умолчанию для параметров, если пользователь не предоставил для них одно значение.</span><span class="sxs-lookup"><span data-stu-id="5d3e5-123">The default parameter set uses default values for parameters if the user does not provide one for them.</span></span> <span data-ttu-id="5d3e5-124">Дополнительные сведения об используемых значениях по умолчанию можно найти в описании указанных ниже параметров.</span><span class="sxs-lookup"><span data-stu-id="5d3e5-124">For more information on the default values used, please see the description for the given parameters below.</span></span>
<span data-ttu-id="5d3e5-125">Этот командлет может назначать роль участнику службы с `Role` параметрами и и `Scope` Параметры; если ни один из этих параметров не указан, роль участника-службы назначена не будет.</span><span class="sxs-lookup"><span data-stu-id="5d3e5-125">This cmdlet has the ability to assign a role to the service principal with the `Role` and `Scope` parameters; if neither of these parameters are provided, no role will be assigned to the service principal.</span></span> <span data-ttu-id="5d3e5-126">Значения по умолчанию для `Role` `Scope` параметров и параметры "участник" и "текущая подписка" соответственно ( _Примечание_. значения по умолчанию используются только в том случае, если пользователь предоставляет значение для одного из двух параметров, но не для другого).</span><span class="sxs-lookup"><span data-stu-id="5d3e5-126">The default values for the `Role` and `Scope` parameters are "Contributor" and the current subscription, respectively ( _note_ : the defaults are only used when the user provides a value for one of the two parameters, but not the other).</span></span>
<span data-ttu-id="5d3e5-127">Командлет также неявно создает приложение и задает его свойства (если свойство ApplicationId не задано).</span><span class="sxs-lookup"><span data-stu-id="5d3e5-127">The cmdlet also implicitly creates an application and sets its properties (if the ApplicationId is not provided).</span></span> <span data-ttu-id="5d3e5-128">Чтобы обновить параметры, зависящие от приложения, используйте командлет Set-AzADApplication.</span><span class="sxs-lookup"><span data-stu-id="5d3e5-128">In order to update the application specific parameters please use Set-AzADApplication cmdlet.</span></span>

> [!WARNING]
> <span data-ttu-id="5d3e5-129">Когда вы создаете участника службы с помощью команды **New-AzADServicePrincipal** , выходные данные включают учетные данные, которые необходимо защитить.</span><span class="sxs-lookup"><span data-stu-id="5d3e5-129">When you create a service principal using the **New-AzADServicePrincipal** command, the output includes credentials that you must protect.</span></span> <span data-ttu-id="5d3e5-130">Убедитесь в том, что эти учетные данные не включены в код, или проверьте учетные данные в системе управления версиями.</span><span class="sxs-lookup"><span data-stu-id="5d3e5-130">Be sure that you do not include these credentials in your code or check the credentials into your source control.</span></span> <span data-ttu-id="5d3e5-131">В качестве альтернативы можно использовать [управляемые удостоверения](/azure/active-directory/managed-identities-azure-resources/overview) , чтобы избежать необходимости использовать учетные данные.</span><span class="sxs-lookup"><span data-stu-id="5d3e5-131">As an alternative, consider using [managed identities](/azure/active-directory/managed-identities-azure-resources/overview) to avoid the need to use credentials.</span></span>
>
> <span data-ttu-id="5d3e5-132">По умолчанию в разделе **New-AzADServicePrincipal** назначается [роль "участник"](/azure/role-based-access-control/built-in-roles#contributor) для субъекта-службы в области подписки.</span><span class="sxs-lookup"><span data-stu-id="5d3e5-132">By default, **New-AzADServicePrincipal** assigns the [Contributor](/azure/role-based-access-control/built-in-roles#contributor) role to the service principal at the subscription scope.</span></span> <span data-ttu-id="5d3e5-133">Чтобы уменьшить риск скомпрометированного субъекта-службы, назначайте более конкретные роли и ограничьте область ресурсом или группой ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5d3e5-133">To reduce your risk of a compromised service principal, assign a more specific role and narrow the scope to a resource or resource group.</span></span> <span data-ttu-id="5d3e5-134">Дополнительные сведения [можно найти в разделе инструкции по добавлению назначения роли](/azure/role-based-access-control/role-assignments-steps) .</span><span class="sxs-lookup"><span data-stu-id="5d3e5-134">See [Steps to add a role assignment](/azure/role-based-access-control/role-assignments-steps) for more information.</span></span>

## <span data-ttu-id="5d3e5-135">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5d3e5-135">EXAMPLES</span></span>

### <span data-ttu-id="5d3e5-136">Пример 1: Создание участника простой службы AD</span><span class="sxs-lookup"><span data-stu-id="5d3e5-136">Example 1 - Simple AD service principal creation</span></span>

```
PS C:\> New-AzADServicePrincipal

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal
```

<span data-ttu-id="5d3e5-137">Приведенная выше команда создает участника службы AD, используя значения по умолчанию для параметров, которые не указаны.</span><span class="sxs-lookup"><span data-stu-id="5d3e5-137">The above command creates an AD service principal using default values for parameters not provided.</span></span> <span data-ttu-id="5d3e5-138">Так как идентификатор приложения не предоставлен, приложение было создано для субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="5d3e5-138">Since an application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="5d3e5-139">Так как никаких значений не было предоставлено `Role` или у `Scope` созданного субъекта-службы нет разрешений.</span><span class="sxs-lookup"><span data-stu-id="5d3e5-139">Since no values were provided for `Role` or `Scope`, the created service principal does not have any permissions.</span></span>

### <span data-ttu-id="5d3e5-140">Пример 2-простого создания участника службы AD с указанной ролью и областью по умолчанию</span><span class="sxs-lookup"><span data-stu-id="5d3e5-140">Example 2 - Simple AD service principal creation with a specified role and default scope</span></span>

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

<span data-ttu-id="5d3e5-141">Приведенная выше команда создает участника службы AD, используя значения по умолчанию для параметров, которые не указаны.</span><span class="sxs-lookup"><span data-stu-id="5d3e5-141">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="5d3e5-142">Так как идентификатор приложения не предоставлен, приложение было создано для субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="5d3e5-142">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="5d3e5-143">Субъект-служба создан с разрешениями "читатель" на текущую подписку (так как для параметра не было предоставлено значение `Scope` ).</span><span class="sxs-lookup"><span data-stu-id="5d3e5-143">The service principal was created with "Reader" permissions over the current subscription (since no value was provided for the `Scope` parameter).</span></span>

### <span data-ttu-id="5d3e5-144">Пример 3-Создание участника службы AD с указанной областью и ролью по умолчанию</span><span class="sxs-lookup"><span data-stu-id="5d3e5-144">Example 3 - Simple AD service principal creation with a specified scope and default role</span></span>

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

<span data-ttu-id="5d3e5-145">Приведенная выше команда создает участника службы AD, используя значения по умолчанию для параметров, которые не указаны.</span><span class="sxs-lookup"><span data-stu-id="5d3e5-145">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="5d3e5-146">Так как идентификатор приложения не предоставлен, приложение было создано для субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="5d3e5-146">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="5d3e5-147">Субъект-служба создан с разрешениями "участник" (так как для параметра не было предоставлено значение `Role` ) для указанной области группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5d3e5-147">The service principal was created with "Contributor" permissions (since no value was provided for the `Role` parameter) over the provided resource group scope.</span></span>

### <span data-ttu-id="5d3e5-148">Пример 4: Создание участника службы AD с указанной областью и ролью</span><span class="sxs-lookup"><span data-stu-id="5d3e5-148">Example 4 - Simple AD service principal creation with a specified scope and role</span></span>

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

<span data-ttu-id="5d3e5-149">Приведенная выше команда создает участника службы AD, используя значения по умолчанию для параметров, которые не указаны.</span><span class="sxs-lookup"><span data-stu-id="5d3e5-149">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="5d3e5-150">Так как идентификатор приложения не предоставлен, приложение было создано для субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="5d3e5-150">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="5d3e5-151">Субъект-служба создан с разрешениями "читатель" в указанной области группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5d3e5-151">The service principal was created with "Reader" permissions over the provided resource group scope.</span></span>

### <span data-ttu-id="5d3e5-152">Пример 5: Создание участника службы AD с помощью идентификатора приложения с назначением роли</span><span class="sxs-lookup"><span data-stu-id="5d3e5-152">Example 5 - Create a new AD service principal using application id with role assignment</span></span>

```
PS C:\> New-AzADServicePrincipal -ApplicationId 34a28ad2-dec4-4a41-bc3b-d22ddf90000e

ServicePrincipalNames : {34a28ad2-dec4-4a41-bc3b-d22ddf90000e, http://my-temp-app}
ApplicationId         : 34a28ad2-dec4-4a41-bc3b-d22ddf90000e
DisplayName           : my-temp-app
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal
```

<span data-ttu-id="5d3e5-153">Создание субъекта-службы AD для приложения с идентификатором приложения "34a28ad2-dec4-4a41-bc3b-d22ddf90000e".</span><span class="sxs-lookup"><span data-stu-id="5d3e5-153">Creates a new AD service principal for the application with application id '34a28ad2-dec4-4a41-bc3b-d22ddf90000e'.</span></span> <span data-ttu-id="5d3e5-154">Так как никаких значений не было предоставлено `Role` или у `Scope` созданного субъекта-службы нет разрешений.</span><span class="sxs-lookup"><span data-stu-id="5d3e5-154">Since no values were provided for `Role` or `Scope`, the created service principal does not have any permissions.</span></span>

### <span data-ttu-id="5d3e5-155">Пример 6: Создание участника службы AD с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="5d3e5-155">Example 6 - Create a new AD service principal using piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId 3ede3c26-b443-4e0b-9efc-b05e68338dc3 | New-AzADServicePrincipal
```

<span data-ttu-id="5d3e5-156">Возвращает приложение с идентификатором объекта "3ede3c26-b443-4e0b-9efc-b05e68338dc3" и каналами, которые можно создать с помощью командлета New-AzADServicePrincipal для создания субъекта-службы AD для этого приложения.</span><span class="sxs-lookup"><span data-stu-id="5d3e5-156">Gets the application with object id '3ede3c26-b443-4e0b-9efc-b05e68338dc3' and pipes that to the New-AzADServicePrincipal cmdlet to create a new AD service principal for that application.</span></span>

## <span data-ttu-id="5d3e5-157">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5d3e5-157">PARAMETERS</span></span>

### <span data-ttu-id="5d3e5-158">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="5d3e5-158">-ApplicationId</span></span>
<span data-ttu-id="5d3e5-159">Уникальный идентификатор приложения для субъекта-службы в клиенте.</span><span class="sxs-lookup"><span data-stu-id="5d3e5-159">The unique application id for a service principal in a tenant.</span></span>
<span data-ttu-id="5d3e5-160">После создания это свойство невозможно изменить.</span><span class="sxs-lookup"><span data-stu-id="5d3e5-160">Once created this property cannot be changed.</span></span>
<span data-ttu-id="5d3e5-161">Если идентификатор приложения не указан, будет создан один из них.</span><span class="sxs-lookup"><span data-stu-id="5d3e5-161">If an application id is not specified, one will be generated.</span></span>

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

### <span data-ttu-id="5d3e5-162">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="5d3e5-162">-ApplicationObject</span></span>
<span data-ttu-id="5d3e5-163">Объект, представляющий приложение, для которого создается субъект-служба.</span><span class="sxs-lookup"><span data-stu-id="5d3e5-163">The object representing the application for which the service principal is created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectWithoutCredentialParameterSet, ApplicationObjectWithPasswordPlainParameterSet, ApplicationObjectWithPasswordCredentialParameterSet, ApplicationObjectWithKeyPlainParameterSet, ApplicationObjectWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5d3e5-164">-CertValue</span><span class="sxs-lookup"><span data-stu-id="5d3e5-164">-CertValue</span></span>
<span data-ttu-id="5d3e5-165">Значение типа учетных данных "асимметричный".</span><span class="sxs-lookup"><span data-stu-id="5d3e5-165">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="5d3e5-166">Он представляет сертификат базового 64 в кодировке.</span><span class="sxs-lookup"><span data-stu-id="5d3e5-166">It represents the base 64 encoded certificate.</span></span>

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

### <span data-ttu-id="5d3e5-167">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d3e5-167">-DefaultProfile</span></span>
<span data-ttu-id="5d3e5-168">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="5d3e5-168">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5d3e5-169">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="5d3e5-169">-DisplayName</span></span>
<span data-ttu-id="5d3e5-170">Понятное имя субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="5d3e5-170">The friendly name of the service principal.</span></span> <span data-ttu-id="5d3e5-171">Если отображаемое имя не задано, это значение будет использоваться по умолчанию: "Azure-PowerShell-MM-DD-гггг-чч-мм-СС", где суффикс — это время создания приложения.</span><span class="sxs-lookup"><span data-stu-id="5d3e5-171">If a display name is not provided, this value will default to 'azure-powershell-MM-dd-yyyy-HH-mm-ss', where the suffix is the time of application creation.</span></span>

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

### <span data-ttu-id="5d3e5-172">-EndDate</span><span class="sxs-lookup"><span data-stu-id="5d3e5-172">-EndDate</span></span>
<span data-ttu-id="5d3e5-173">Эффективная дата окончания использования учетных данных.</span><span class="sxs-lookup"><span data-stu-id="5d3e5-173">The effective end date of the credential usage.</span></span>
<span data-ttu-id="5d3e5-174">Значение даты окончания по умолчанию — это год от сегодняшнего дня.</span><span class="sxs-lookup"><span data-stu-id="5d3e5-174">The default end date value is one year from today.</span></span> <span data-ttu-id="5d3e5-175">Для «асимметричных» учетных данных типа это значение должно быть установлено в on или до даты, когда сертификат X509 является действительным.</span><span class="sxs-lookup"><span data-stu-id="5d3e5-175">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="5d3e5-176">-KeyCredential</span><span class="sxs-lookup"><span data-stu-id="5d3e5-176">-KeyCredential</span></span>
<span data-ttu-id="5d3e5-177">Коллекция ключевых учетных данных, связанных с приложением.</span><span class="sxs-lookup"><span data-stu-id="5d3e5-177">The collection of key credentials associated with the application.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]
Parameter Sets: ApplicationWithKeyCredentialParameterSet, DisplayNameWithKeyCredentialParameterSet
Aliases: KeyCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]
Parameter Sets: ApplicationObjectWithKeyCredentialParameterSet
Aliases: KeyCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d3e5-178">-PasswordCredential</span><span class="sxs-lookup"><span data-stu-id="5d3e5-178">-PasswordCredential</span></span>
<span data-ttu-id="5d3e5-179">Коллекция учетных данных пароля, связанных с приложением.</span><span class="sxs-lookup"><span data-stu-id="5d3e5-179">The collection of password credentials associated with the application.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]
Parameter Sets: ApplicationWithPasswordCredentialParameterSet, DisplayNameWithPasswordCredentialParameterSet
Aliases: PasswordCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]
Parameter Sets: ApplicationObjectWithPasswordCredentialParameterSet
Aliases: PasswordCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d3e5-180">-Role (роль)</span><span class="sxs-lookup"><span data-stu-id="5d3e5-180">-Role</span></span>
<span data-ttu-id="5d3e5-181">Роль, которую участник службы имеет над областью.</span><span class="sxs-lookup"><span data-stu-id="5d3e5-181">The role that the service principal has over the scope.</span></span> <span data-ttu-id="5d3e5-182">Если задано значение, `Scope` но для него не указано значение `Role` , `Role` по умолчанию будет использоваться роль "участник".</span><span class="sxs-lookup"><span data-stu-id="5d3e5-182">If a value for `Scope` is provided, but no value is provided for `Role`, then `Role` will default to the 'Contributor' role.</span></span>

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

### <span data-ttu-id="5d3e5-183">-Scope</span><span class="sxs-lookup"><span data-stu-id="5d3e5-183">-Scope</span></span>
<span data-ttu-id="5d3e5-184">Область, для которой предоставлены разрешения субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="5d3e5-184">The scope that the service principal has permissions on.</span></span> <span data-ttu-id="5d3e5-185">Если задано значение, `Role` но для него не указано значение `Scope` , `Scope` по умолчанию будет использоваться текущая подписка.</span><span class="sxs-lookup"><span data-stu-id="5d3e5-185">If a value for `Role` is provided, but no value is provided for `Scope`, then `Scope` will default to the current subscription.</span></span>

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

### <span data-ttu-id="5d3e5-186">-SkipAssignment</span><span class="sxs-lookup"><span data-stu-id="5d3e5-186">-SkipAssignment</span></span>
<span data-ttu-id="5d3e5-187">Если задано значение, будет пропущено создание назначения роли по умолчанию для субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="5d3e5-187">If set, will skip creating the default role assignment for the service principal.</span></span>

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

### <span data-ttu-id="5d3e5-188">-StartDate</span><span class="sxs-lookup"><span data-stu-id="5d3e5-188">-StartDate</span></span>
<span data-ttu-id="5d3e5-189">Фактическая дата начала использования учетных данных.</span><span class="sxs-lookup"><span data-stu-id="5d3e5-189">The effective start date of the credential usage.</span></span>
<span data-ttu-id="5d3e5-190">Значение даты начала по умолчанию — сегодня.</span><span class="sxs-lookup"><span data-stu-id="5d3e5-190">The default start date value is today.</span></span> <span data-ttu-id="5d3e5-191">Для «асимметричных» учетных данных типа это значение должно быть задано как on или после даты, с которой сертификат X509 является действительным.</span><span class="sxs-lookup"><span data-stu-id="5d3e5-191">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="5d3e5-192">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5d3e5-192">-Confirm</span></span>
<span data-ttu-id="5d3e5-193">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5d3e5-193">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d3e5-194">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d3e5-194">-WhatIf</span></span>
<span data-ttu-id="5d3e5-195">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5d3e5-195">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d3e5-196">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5d3e5-196">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d3e5-197">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d3e5-197">CommonParameters</span></span>
<span data-ttu-id="5d3e5-198">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5d3e5-198">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d3e5-199">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d3e5-199">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d3e5-200">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5d3e5-200">INPUTS</span></span>

### <span data-ttu-id="5d3e5-201">System. GUID</span><span class="sxs-lookup"><span data-stu-id="5d3e5-201">System.Guid</span></span>

### <span data-ttu-id="5d3e5-202">System. String</span><span class="sxs-lookup"><span data-stu-id="5d3e5-202">System.String</span></span>

### <span data-ttu-id="5d3e5-203">Microsoft. Azure. Commands. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="5d3e5-203">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

### <span data-ttu-id="5d3e5-204">Microsoft. Azure. Commands. ActiveDirectory. PSADPasswordCredential []</span><span class="sxs-lookup"><span data-stu-id="5d3e5-204">Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]</span></span>

### <span data-ttu-id="5d3e5-205">Microsoft. Azure. Commands. ActiveDirectory. PSADKeyCredential []</span><span class="sxs-lookup"><span data-stu-id="5d3e5-205">Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]</span></span>

### <span data-ttu-id="5d3e5-206">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="5d3e5-206">System.DateTime</span></span>

## <span data-ttu-id="5d3e5-207">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5d3e5-207">OUTPUTS</span></span>

### <span data-ttu-id="5d3e5-208">Microsoft. Azure. Commands. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="5d3e5-208">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="5d3e5-209">Microsoft. Azure. Commands. Resources. Authorization. PSADServicePrincipalWrapper</span><span class="sxs-lookup"><span data-stu-id="5d3e5-209">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADServicePrincipalWrapper</span></span>

## <span data-ttu-id="5d3e5-210">Пуск</span><span class="sxs-lookup"><span data-stu-id="5d3e5-210">NOTES</span></span>
<span data-ttu-id="5d3e5-211">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, ресурс, группа, шаблон, развертывание</span><span class="sxs-lookup"><span data-stu-id="5d3e5-211">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="5d3e5-212">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5d3e5-212">RELATED LINKS</span></span>

[<span data-ttu-id="5d3e5-213">Remove-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="5d3e5-213">Remove-AzADServicePrincipal</span></span>](./Remove-AzADServicePrincipal.md)

[<span data-ttu-id="5d3e5-214">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="5d3e5-214">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

[<span data-ttu-id="5d3e5-215">New-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="5d3e5-215">New-AzADApplication</span></span>](./New-AzADApplication.md)

[<span data-ttu-id="5d3e5-216">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="5d3e5-216">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="5d3e5-217">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="5d3e5-217">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

[<span data-ttu-id="5d3e5-218">New-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="5d3e5-218">New-AzADSpCredential</span></span>](./New-AzADSpCredential.md)

[<span data-ttu-id="5d3e5-219">Remove-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="5d3e5-219">Remove-AzADSpCredential</span></span>](./Remove-AzADSpCredential.md)

