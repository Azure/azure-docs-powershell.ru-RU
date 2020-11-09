---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D602F910-B26F-473D-B5B6-C7BDFB0A14CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
ms.openlocfilehash: 6d268c2378c93bcfb98e64c654880e8055bcede8
ms.sourcegitcommit: 375232b84336ef5e13052504deaa43f5bd4b7f65
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/05/2020
ms.locfileid: "94319472"
---
# <span data-ttu-id="18370-101">New-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="18370-101">New-AzADServicePrincipal</span></span>

## <span data-ttu-id="18370-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="18370-102">SYNOPSIS</span></span>
<span data-ttu-id="18370-103">Создание нового субъекта-службы Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="18370-103">Creates a new Azure active directory service principal.</span></span>

## <span data-ttu-id="18370-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="18370-104">SYNTAX</span></span>

### <span data-ttu-id="18370-105">SimpleParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="18370-105">SimpleParameterSet (Default)</span></span>

```
New-AzADServicePrincipal [-ApplicationId <Guid>] [-DisplayName <String>] [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-Scope <String>] [-Role <String>] [-SkipAssignment]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18370-106">ApplicationWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="18370-106">ApplicationWithoutCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="18370-107">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="18370-107">ApplicationWithPasswordPlainParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationId <Guid> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18370-108">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="18370-108">ApplicationWithPasswordCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationId <Guid> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18370-109">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="18370-109">ApplicationWithKeyPlainParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationId <Guid> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18370-110">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="18370-110">ApplicationWithKeyCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationId <Guid> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18370-111">DisplayNameWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="18370-111">DisplayNameWithoutCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="18370-112">DisplayNameWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="18370-112">DisplayNameWithPasswordPlainParameterSet</span></span>

```
New-AzADServicePrincipal -DisplayName <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18370-113">DisplayNameWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="18370-113">DisplayNameWithPasswordCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -DisplayName <String> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18370-114">DisplayNameWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="18370-114">DisplayNameWithKeyPlainParameterSet</span></span>

```
New-AzADServicePrincipal -DisplayName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18370-115">DisplayNameWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="18370-115">DisplayNameWithKeyCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -DisplayName <String> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18370-116">ApplicationObjectWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="18370-116">ApplicationObjectWithPasswordPlainParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18370-117">ApplicationObjectWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="18370-117">ApplicationObjectWithPasswordCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18370-118">ApplicationObjectWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="18370-118">ApplicationObjectWithKeyPlainParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18370-119">ApplicationObjectWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="18370-119">ApplicationObjectWithKeyCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18370-120">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="18370-120">DESCRIPTION</span></span>

<span data-ttu-id="18370-121">Создание нового субъекта-службы Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="18370-121">Creates a new Azure active directory service principal.</span></span> <span data-ttu-id="18370-122">Параметр по умолчанию использует значения по умолчанию для параметров, если они не заданы.</span><span class="sxs-lookup"><span data-stu-id="18370-122">The default parameter set uses default values for parameters if they are not provided.</span></span> <span data-ttu-id="18370-123">Дополнительные сведения о значениях по умолчанию можно найти в описании каждого параметра.</span><span class="sxs-lookup"><span data-stu-id="18370-123">For more information on default values, see the description for each parameter.</span></span> <span data-ttu-id="18370-124">Этот командлет может назначать роль субъекту-службы с параметрами **роли** и **области** .</span><span class="sxs-lookup"><span data-stu-id="18370-124">This cmdlet has the ability to assign a role to the service principal with the **Role** and **Scope** parameters.</span></span> <span data-ttu-id="18370-125">Если оба аргумента опущены, роль участника назначается участнику службы.</span><span class="sxs-lookup"><span data-stu-id="18370-125">If both are omitted, the contributor role is assigned to the service principal.</span></span> <span data-ttu-id="18370-126">Значения по умолчанию для **роли** и параметров **области** являются **сотрудниками** текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="18370-126">The default values for the **Role** and **Scope** parameters are **Contributor** for the current subscription.</span></span> <span data-ttu-id="18370-127">Командлет создает приложение и задает его свойства, если не задано значение ApplicationId.</span><span class="sxs-lookup"><span data-stu-id="18370-127">The cmdlet creates an application and sets its properties if an ApplicationId is not provided.</span></span> <span data-ttu-id="18370-128">Чтобы обновить параметры, зависящие от приложения, используйте командлет [Update-AzADApplication](./update-azadapplication.md) .</span><span class="sxs-lookup"><span data-stu-id="18370-128">To update the application-specific parameters, use the [Update-AzADApplication](./update-azadapplication.md) cmdlet.</span></span>

> [!WARNING]
> <span data-ttu-id="18370-129">Когда вы создаете участника службы с помощью команды **New-AzADServicePrincipal** , выходные данные включают учетные данные, которые необходимо защитить.</span><span class="sxs-lookup"><span data-stu-id="18370-129">When you create a service principal using the **New-AzADServicePrincipal** command, the output includes credentials that you must protect.</span></span> <span data-ttu-id="18370-130">Убедитесь в том, что эти учетные данные не включены в код, или проверьте учетные данные в системе управления версиями.</span><span class="sxs-lookup"><span data-stu-id="18370-130">Be sure that you do not include these credentials in your code or check the credentials into your source control.</span></span> <span data-ttu-id="18370-131">В качестве альтернативы можно использовать [управляемые удостоверения](/azure/active-directory/managed-identities-azure-resources/overview) , чтобы избежать необходимости использовать учетные данные.</span><span class="sxs-lookup"><span data-stu-id="18370-131">As an alternative, consider using [managed identities](/azure/active-directory/managed-identities-azure-resources/overview) to avoid the need to use credentials.</span></span>
>
> <span data-ttu-id="18370-132">По умолчанию в разделе **New-AzADServicePrincipal** назначается [роль "участник"](/azure/role-based-access-control/built-in-roles#contributor) для субъекта-службы в области подписки.</span><span class="sxs-lookup"><span data-stu-id="18370-132">By default, **New-AzADServicePrincipal** assigns the [Contributor](/azure/role-based-access-control/built-in-roles#contributor) role to the service principal at the subscription scope.</span></span> <span data-ttu-id="18370-133">Чтобы уменьшить риск скомпрометированного субъекта-службы, назначайте более конкретные роли и ограничьте область ресурсом или группой ресурсов.</span><span class="sxs-lookup"><span data-stu-id="18370-133">To reduce your risk of a compromised service principal, assign a more specific role and narrow the scope to a resource or resource group.</span></span> <span data-ttu-id="18370-134">Дополнительные сведения [можно найти в разделе инструкции по добавлению назначения роли](/azure/role-based-access-control/role-assignments-steps) .</span><span class="sxs-lookup"><span data-stu-id="18370-134">See [Steps to add a role assignment](/azure/role-based-access-control/role-assignments-steps) for more information.</span></span>

## <span data-ttu-id="18370-135">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="18370-135">EXAMPLES</span></span>

### <span data-ttu-id="18370-136">Пример 1: Создание участника простой службы AD</span><span class="sxs-lookup"><span data-stu-id="18370-136">Example 1: Simple AD service principal creation</span></span>

<span data-ttu-id="18370-137">В следующем примере создается субъект-служба AD с использованием значений по умолчанию для параметров, которые не указаны.</span><span class="sxs-lookup"><span data-stu-id="18370-137">The following example creates an AD service principal using default values for parameters not specified.</span></span> <span data-ttu-id="18370-138">Так как идентификатор приложения не предоставляется, для него создается приложение для субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="18370-138">Since an application ID is not provided, an application is created for the service principal.</span></span> <span data-ttu-id="18370-139">Так как для **роли** или **области** не предоставлены значения, созданному участнику службы назначается роль **участника** для текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="18370-139">Since no values are provided for **Role** or **Scope** , the created service principal is assigned the **contributor** role for the current subscription.</span></span>

```powershell
New-AzADServicePrincipal
```

```Output
Secret                : System.Security.SecureString
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : 00000000-0000-0000-0000-000000000000
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : 00000000-0000-0000-0000-000000000000
Type                  : ServicePrincipal
```

### <span data-ttu-id="18370-140">Пример 2: Создание участника простой службы AD с указанной ролью и областью по умолчанию</span><span class="sxs-lookup"><span data-stu-id="18370-140">Example 2: Simple AD service principal creation with a specified role and default scope</span></span>

<span data-ttu-id="18370-141">В следующем примере создается субъект-служба AD с использованием значений по умолчанию для параметров, которые не указаны.</span><span class="sxs-lookup"><span data-stu-id="18370-141">The following example creates an AD service principal using the default values for parameters not specified.</span></span> <span data-ttu-id="18370-142">Так как идентификатор приложения не предоставляется, для него создается приложение для субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="18370-142">Since the application ID is not provided, an application is created for the service principal.</span></span> <span data-ttu-id="18370-143">Субъект-служба создается с разрешениями на **Чтение** для текущей подписки, так как для параметра **Scope** не задано значение.</span><span class="sxs-lookup"><span data-stu-id="18370-143">The service principal is created with **Reader** permissions for the current subscription since no value is provided for the **Scope** parameter.</span></span>

```powershell
New-AzADServicePrincipal -Role Reader
```

```Output
Secret                : System.Security.SecureString
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : 00000000-0000-0000-0000-000000000000
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : 00000000-0000-0000-0000-000000000000
Type                  : ServicePrincipal

WARNING: Assigning role 'Reader' over scope '/subscriptions/00000000-0000-0000-0000-000000000000' to the new service principal.
```

### <span data-ttu-id="18370-144">Пример 3: Создание участника простой службы AD с заданной областью и ролью по умолчанию</span><span class="sxs-lookup"><span data-stu-id="18370-144">Example 3: Simple AD service principal creation with a specified scope and default role</span></span>

<span data-ttu-id="18370-145">В следующем примере создается субъект-служба AD с использованием значений по умолчанию для параметров, которые не указаны.</span><span class="sxs-lookup"><span data-stu-id="18370-145">The following example creates an AD service principal using the default values for parameters not specified.</span></span> <span data-ttu-id="18370-146">Так как идентификатор приложения не предоставляется, для него создается приложение для субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="18370-146">Since the application ID is not provided, an application is created for the service principal.</span></span> <span data-ttu-id="18370-147">Субъект-служба создается с разрешениями **участника** для указанной области группы ресурсов, так как для параметра **Role** не задано значение.</span><span class="sxs-lookup"><span data-stu-id="18370-147">The service principal is created with **Contributor** permissions for the provided resource group scope since no value is provided for the **Role** parameter.</span></span>

```powershell
New-AzADServicePrincipal -Scope /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myResourceGroup
```

```Output
Secret                : System.Security.SecureString
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : 00000000-0000-0000-0000-000000000000
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : 00000000-0000-0000-0000-000000000000
Type                  : ServicePrincipal

WARNING: Assigning role 'Contributor' over scope '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myResourceGroup' to the new service principal.
```

### <span data-ttu-id="18370-148">Пример 4: Создание участника простой службы AD с указанной областью и ролью</span><span class="sxs-lookup"><span data-stu-id="18370-148">Example 4: Simple AD service principal creation with a specified scope and role</span></span>

<span data-ttu-id="18370-149">В следующем примере создается субъект-служба AD с использованием значений по умолчанию для параметров, которые не указаны.</span><span class="sxs-lookup"><span data-stu-id="18370-149">The following example creates an AD service principal using the default values for parameters not specified.</span></span> <span data-ttu-id="18370-150">Так как идентификатор приложения не предоставляется, для него создается приложение для субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="18370-150">Since the application ID is not provided, an application is created for the service principal.</span></span> <span data-ttu-id="18370-151">Субъект-служба создается с разрешениями на **Чтение** для указанной области группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="18370-151">The service principal is created with **Reader** permissions for the provided resource group scope.</span></span>

```powershell
New-AzADServicePrincipal -Role Reader -Scope /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myResourceGroup
```

```Output
Secret                : System.Security.SecureString
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : 00000000-0000-0000-0000-000000000000
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : 00000000-0000-0000-0000-000000000000
Type                  : ServicePrincipal

WARNING: Assigning role 'Reader' over scope '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myResourceGroup' to the new service principal.
```

### <span data-ttu-id="18370-152">Пример 5: Создание участника службы AD с помощью идентификатора приложения с назначением роли</span><span class="sxs-lookup"><span data-stu-id="18370-152">Example 5: Create a new AD service principal using application ID with role assignment</span></span>

<span data-ttu-id="18370-153">В следующем примере создается субъект-служба AD для приложения с ИДЕНТИФИКАТОРом приложения "00000000-0000-0000-0000-000000000000".</span><span class="sxs-lookup"><span data-stu-id="18370-153">The following example creates a new AD service principal for the application with application ID '00000000-0000-0000-0000-000000000000'.</span></span> <span data-ttu-id="18370-154">Так как для **роли** или **области** не предоставлены значения, созданному участнику службы назначается роль **участника** для текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="18370-154">Since no values are provided for **Role** or **Scope** , the created service principal is assigned the **contributor** role for the current subscription.</span></span>

```powershell
New-AzADServicePrincipal -ApplicationId 00000000-0000-0000-0000-000000000000
```

```Output
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://my-temp-app}
ApplicationId         : 00000000-0000-0000-0000-000000000000
DisplayName           : my-temp-app
Id                    : 00000000-0000-0000-0000-000000000000
Type                  : ServicePrincipal
```

### <span data-ttu-id="18370-155">Пример 6: создание нового участника службы AD с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="18370-155">Example 6: Create a new AD service principal using piping</span></span>

<span data-ttu-id="18370-156">В следующем примере извлекается приложение с ИДЕНТИФИКАТОРом объекта "3ede3c26-b443-4e0b-9efc-b05e68338dc3" с помощью командлета [Get-AzADApplication](./get-azadapplication.md) .</span><span class="sxs-lookup"><span data-stu-id="18370-156">The following example retrieves the application with object ID '3ede3c26-b443-4e0b-9efc-b05e68338dc3' using the [Get-AzADApplication](./get-azadapplication.md) cmdlet.</span></span> <span data-ttu-id="18370-157">Результаты будут переданы `New-AzADServicePrincipal` командлету для создания нового субъекта-службы для этого приложения.</span><span class="sxs-lookup"><span data-stu-id="18370-157">The results are piped to the `New-AzADServicePrincipal` cmdlet to create a new AD service principal for that application.</span></span>

```powershell
Get-AzADApplication -ObjectId 3ede3c26-b443-4e0b-9efc-b05e68338dc3 | New-AzADServicePrincipal
```

### <span data-ttu-id="18370-158">Пример 7: Создание участника службы AD с использованием DisplayName и учетных данных пароля</span><span class="sxs-lookup"><span data-stu-id="18370-158">Example 7: Create a new AD service principal using DisplayName and password credential</span></span>

<span data-ttu-id="18370-159">В следующем примере создается новое приложение **с именем "** имя для" и пароль для **StrongPassworld! 23**.</span><span class="sxs-lookup"><span data-stu-id="18370-159">The following example creates a new application with the name **ServicePrincipalName** and a password of **StrongPassworld!23**.</span></span> <span data-ttu-id="18370-160">Он создает субъект-службу на основе созданного приложения.</span><span class="sxs-lookup"><span data-stu-id="18370-160">It creates the service principal based on the created application.</span></span> <span data-ttu-id="18370-161">Дата начала и Дата окончания добавляются в учетные данные пароля.</span><span class="sxs-lookup"><span data-stu-id="18370-161">The start date and end date are added to the password credential.</span></span>

```powershell
$credentials = New-Object -TypeName Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential -Property @{
  StartDate=Get-Date; EndDate=Get-Date -Year 2024; Password='StrongPassworld!23'}
$sp = New-AzAdServicePrincipal -DisplayName ServicePrincipalName -PasswordCredential $credentials
```

```Output
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://ServicePrincipalName}
ApplicationId         : 00000000-0000-0000-0000-000000000000c
ObjectType            : ServicePrincipal
DisplayName           : ServicePrincipalName
Id                    : 00000000-0000-0000-0000-000000000000
Type                  :
```

### <span data-ttu-id="18370-162">Пример 8: создание субъекта-службы AD с использованием учетных данных DisplayName и открытого ключа</span><span class="sxs-lookup"><span data-stu-id="18370-162">Example 8: Create a new AD service principal using DisplayName and plain key credential</span></span>

<span data-ttu-id="18370-163">В следующем примере создается новое приложение **с именем "** имя программного кода" и **$certом** сертификата. Он создает участника службы на основе созданного приложения.</span><span class="sxs-lookup"><span data-stu-id="18370-163">The following example creates a new application with the name **ServicePrincipalName** and a certificate **$cert**. It creates the service principal based on the application created.</span></span> <span data-ttu-id="18370-164">Дата окончания добавляется к учетным данным ключа.</span><span class="sxs-lookup"><span data-stu-id="18370-164">The end date is added to key credential.</span></span>

```powershell
$cert = 'public certificate as Base64 encoded string'
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -CertValue $cert  -EndDate '2021-01-01'
```

```Output
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://ServicePrincipalName}
ApplicationId         : 00000000-0000-0000-0000-000000000000
ObjectType            : ServicePrincipal
DisplayName           : ServicePrincipalName
Id                    : 00000000-0000-0000-0000-000000000000
Type                  :
```

## <span data-ttu-id="18370-165">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="18370-165">PARAMETERS</span></span>

### <span data-ttu-id="18370-166">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="18370-166">-ApplicationId</span></span>

<span data-ttu-id="18370-167">Уникальный идентификатор приложения для субъекта-службы в клиенте.</span><span class="sxs-lookup"><span data-stu-id="18370-167">The unique application ID for a service principal in a tenant.</span></span> <span data-ttu-id="18370-168">После создания это свойство невозможно изменить.</span><span class="sxs-lookup"><span data-stu-id="18370-168">Once created this property cannot be changed.</span></span> <span data-ttu-id="18370-169">Если идентификатор приложения для существующего приложения не указан, создается приложение.</span><span class="sxs-lookup"><span data-stu-id="18370-169">If an application ID for an existing application is not specified, an application is created.</span></span>

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

### <span data-ttu-id="18370-170">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="18370-170">-ApplicationObject</span></span>

<span data-ttu-id="18370-171">Объект, представляющий приложение, для которого создается субъект-служба.</span><span class="sxs-lookup"><span data-stu-id="18370-171">The object representing the application for which the service principal is created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectWithPasswordPlainParameterSet, ApplicationObjectWithPasswordCredentialParameterSet, ApplicationObjectWithKeyPlainParameterSet, ApplicationObjectWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="18370-172">-CertValue</span><span class="sxs-lookup"><span data-stu-id="18370-172">-CertValue</span></span>

<span data-ttu-id="18370-173">Значение типа асимметричных учетных данных.</span><span class="sxs-lookup"><span data-stu-id="18370-173">The value of the asymmetric credential type.</span></span> <span data-ttu-id="18370-174">Он представляет сертификат в кодировке Base64.</span><span class="sxs-lookup"><span data-stu-id="18370-174">It represents the Base64 encoded certificate.</span></span>

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

### <span data-ttu-id="18370-175">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18370-175">-DefaultProfile</span></span>

<span data-ttu-id="18370-176">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="18370-176">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18370-177">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="18370-177">-DisplayName</span></span>

<span data-ttu-id="18370-178">Понятное имя субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="18370-178">The friendly name of the service principal.</span></span> <span data-ttu-id="18370-179">Если отображаемое имя не указано, это значение будет использоваться по умолчанию для **Azure-PowerShell-mm-дд-гггг-чч-мм-SS** , где этот суффикс является временем создания приложения.</span><span class="sxs-lookup"><span data-stu-id="18370-179">If a display name is not provided, this value will default to **azure-powershell-MM-dd-yyyy-HH-mm-ss** where the suffix is the time of application creation.</span></span>

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

### <span data-ttu-id="18370-180">-EndDate</span><span class="sxs-lookup"><span data-stu-id="18370-180">-EndDate</span></span>

<span data-ttu-id="18370-181">Эффективная дата окончания использования учетных данных.</span><span class="sxs-lookup"><span data-stu-id="18370-181">The effective end date of the credential usage.</span></span> <span data-ttu-id="18370-182">Значение даты окончания по умолчанию — это год от сегодняшнего дня.</span><span class="sxs-lookup"><span data-stu-id="18370-182">The default end date value is one year from today.</span></span>
<span data-ttu-id="18370-183">Для учетных данных асимметричного типа это значение должно быть установлено в on или до даты, когда сертификат X509 является действительным.</span><span class="sxs-lookup"><span data-stu-id="18370-183">For an asymmetric type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="18370-184">-KeyCredential</span><span class="sxs-lookup"><span data-stu-id="18370-184">-KeyCredential</span></span>

<span data-ttu-id="18370-185">Коллекция ключевых учетных данных, связанных с приложением.</span><span class="sxs-lookup"><span data-stu-id="18370-185">The collection of key credentials associated with the application.</span></span>

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

### <span data-ttu-id="18370-186">-PasswordCredential</span><span class="sxs-lookup"><span data-stu-id="18370-186">-PasswordCredential</span></span>

<span data-ttu-id="18370-187">Коллекция учетных данных пароля, связанных с приложением.</span><span class="sxs-lookup"><span data-stu-id="18370-187">The collection of password credentials associated with the application.</span></span>

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

### <span data-ttu-id="18370-188">-Role (роль)</span><span class="sxs-lookup"><span data-stu-id="18370-188">-Role</span></span>

<span data-ttu-id="18370-189">Роль, которую участник службы имеет над областью.</span><span class="sxs-lookup"><span data-stu-id="18370-189">The role that the service principal has over the scope.</span></span> <span data-ttu-id="18370-190">Если значение не задано, **по умолчанию используется** роль **участника** .</span><span class="sxs-lookup"><span data-stu-id="18370-190">If no value is provided, **Role** defaults to the **Contributor** role.</span></span>

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

### <span data-ttu-id="18370-191">-Scope</span><span class="sxs-lookup"><span data-stu-id="18370-191">-Scope</span></span>

<span data-ttu-id="18370-192">Область, для которой у субъекта-службы есть разрешения.</span><span class="sxs-lookup"><span data-stu-id="18370-192">The scope that the service principal has permissions for.</span></span> <span data-ttu-id="18370-193">Если значение не задано, **по** умолчанию используется текущая подписка.</span><span class="sxs-lookup"><span data-stu-id="18370-193">If no value is provided, **Scope** defaults to the current subscription.</span></span>

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

### <span data-ttu-id="18370-194">-SkipAssignment</span><span class="sxs-lookup"><span data-stu-id="18370-194">-SkipAssignment</span></span>

<span data-ttu-id="18370-195">Если задано, пропускать создание назначения роли по умолчанию для субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="18370-195">If set, skip creating the default role assignment for the service principal.</span></span>

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

### <span data-ttu-id="18370-196">-StartDate</span><span class="sxs-lookup"><span data-stu-id="18370-196">-StartDate</span></span>

<span data-ttu-id="18370-197">Фактическая дата начала использования учетных данных.</span><span class="sxs-lookup"><span data-stu-id="18370-197">The effective start date of the credential usage.</span></span> <span data-ttu-id="18370-198">Значение даты начала по умолчанию — сегодня.</span><span class="sxs-lookup"><span data-stu-id="18370-198">The default start date value is today.</span></span> <span data-ttu-id="18370-199">Для учетных данных асимметричного типа это значение должно быть установлено на on или после даты, с которой сертификат X509 является действительным.</span><span class="sxs-lookup"><span data-stu-id="18370-199">For an asymmetric type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="18370-200">-Confirm</span><span class="sxs-lookup"><span data-stu-id="18370-200">-Confirm</span></span>

<span data-ttu-id="18370-201">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="18370-201">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18370-202">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18370-202">-WhatIf</span></span>

<span data-ttu-id="18370-203">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="18370-203">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="18370-204">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="18370-204">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18370-205">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18370-205">CommonParameters</span></span>
<span data-ttu-id="18370-206">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="18370-206">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18370-207">Дополнительные сведения можно найти в разделе [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span><span class="sxs-lookup"><span data-stu-id="18370-207">For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span></span>
## <span data-ttu-id="18370-208">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="18370-208">INPUTS</span></span>

### <span data-ttu-id="18370-209">System. GUID</span><span class="sxs-lookup"><span data-stu-id="18370-209">System.Guid</span></span>

### <span data-ttu-id="18370-210">System. String</span><span class="sxs-lookup"><span data-stu-id="18370-210">System.String</span></span>

### <span data-ttu-id="18370-211">Microsoft. Azure. Commands. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="18370-211">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

### <span data-ttu-id="18370-212">Microsoft. Azure. Commands. ActiveDirectory. PSADPasswordCredential []</span><span class="sxs-lookup"><span data-stu-id="18370-212">Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]</span></span>

### <span data-ttu-id="18370-213">Microsoft. Azure. Commands. ActiveDirectory. PSADKeyCredential []</span><span class="sxs-lookup"><span data-stu-id="18370-213">Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]</span></span>

### <span data-ttu-id="18370-214">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="18370-214">System.DateTime</span></span>

## <span data-ttu-id="18370-215">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="18370-215">OUTPUTS</span></span>

### <span data-ttu-id="18370-216">Microsoft. Azure. Commands. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="18370-216">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="18370-217">Microsoft. Azure. Commands. Resources. Authorization. PSADServicePrincipalWrapper</span><span class="sxs-lookup"><span data-stu-id="18370-217">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADServicePrincipalWrapper</span></span>

## <span data-ttu-id="18370-218">Пуск</span><span class="sxs-lookup"><span data-stu-id="18370-218">NOTES</span></span>

<span data-ttu-id="18370-219">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, ресурс, группа, шаблон, развертывание</span><span class="sxs-lookup"><span data-stu-id="18370-219">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="18370-220">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="18370-220">RELATED LINKS</span></span>

[<span data-ttu-id="18370-221">Remove-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="18370-221">Remove-AzADServicePrincipal</span></span>](./Remove-AzADServicePrincipal.md)

[<span data-ttu-id="18370-222">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="18370-222">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

[<span data-ttu-id="18370-223">New-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="18370-223">New-AzADApplication</span></span>](./New-AzADApplication.md)

[<span data-ttu-id="18370-224">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="18370-224">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="18370-225">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="18370-225">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

[<span data-ttu-id="18370-226">New-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="18370-226">New-AzADSpCredential</span></span>](./New-AzADSpCredential.md)

[<span data-ttu-id="18370-227">Remove-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="18370-227">Remove-AzADSpCredential</span></span>](./Remove-AzADSpCredential.md)