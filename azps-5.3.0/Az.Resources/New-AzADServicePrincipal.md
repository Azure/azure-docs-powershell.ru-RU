---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D602F910-B26F-473D-B5B6-C7BDFB0A14CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
ms.openlocfilehash: 6d268c2378c93bcfb98e64c654880e8055bcede8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505233"
---
# <span data-ttu-id="d875f-101">New-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="d875f-101">New-AzADServicePrincipal</span></span>

## <span data-ttu-id="d875f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d875f-102">SYNOPSIS</span></span>
<span data-ttu-id="d875f-103">Создает новую главную службу Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d875f-103">Creates a new Azure active directory service principal.</span></span>

## <span data-ttu-id="d875f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d875f-104">SYNTAX</span></span>

### <span data-ttu-id="d875f-105">SimpleParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d875f-105">SimpleParameterSet (Default)</span></span>

```
New-AzADServicePrincipal [-ApplicationId <Guid>] [-DisplayName <String>] [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-Scope <String>] [-Role <String>] [-SkipAssignment]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d875f-106">ApplicationWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="d875f-106">ApplicationWithoutCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d875f-107">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="d875f-107">ApplicationWithPasswordPlainParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationId <Guid> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d875f-108">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="d875f-108">ApplicationWithPasswordCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationId <Guid> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d875f-109">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="d875f-109">ApplicationWithKeyPlainParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationId <Guid> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d875f-110">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="d875f-110">ApplicationWithKeyCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationId <Guid> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d875f-111">DisplayNameWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="d875f-111">DisplayNameWithoutCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d875f-112">DisplayNameWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="d875f-112">DisplayNameWithPasswordPlainParameterSet</span></span>

```
New-AzADServicePrincipal -DisplayName <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d875f-113">DisplayNameWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="d875f-113">DisplayNameWithPasswordCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -DisplayName <String> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d875f-114">DisplayNameWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="d875f-114">DisplayNameWithKeyPlainParameterSet</span></span>

```
New-AzADServicePrincipal -DisplayName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d875f-115">DisplayNameWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="d875f-115">DisplayNameWithKeyCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -DisplayName <String> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d875f-116">ApplicationObjectWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="d875f-116">ApplicationObjectWithPasswordPlainParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d875f-117">ApplicationObjectWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="d875f-117">ApplicationObjectWithPasswordCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d875f-118">ApplicationObjectWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="d875f-118">ApplicationObjectWithKeyPlainParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d875f-119">ApplicationObjectWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="d875f-119">ApplicationObjectWithKeyCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d875f-120">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d875f-120">DESCRIPTION</span></span>

<span data-ttu-id="d875f-121">Создает новую главную службу Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d875f-121">Creates a new Azure active directory service principal.</span></span> <span data-ttu-id="d875f-122">В наборе параметров по умолчанию используются значения по умолчанию для параметров, если они не заданы.</span><span class="sxs-lookup"><span data-stu-id="d875f-122">The default parameter set uses default values for parameters if they are not provided.</span></span> <span data-ttu-id="d875f-123">Дополнительные сведения о значениях по умолчанию см. в описании каждого параметра.</span><span class="sxs-lookup"><span data-stu-id="d875f-123">For more information on default values, see the description for each parameter.</span></span> <span data-ttu-id="d875f-124">С помощью этого cmdlet можно назначить роль главе службы с параметрами **"Роль"** и **"Область".**</span><span class="sxs-lookup"><span data-stu-id="d875f-124">This cmdlet has the ability to assign a role to the service principal with the **Role** and **Scope** parameters.</span></span> <span data-ttu-id="d875f-125">Если обе функции опущены, роль участника назначена участнику службы.</span><span class="sxs-lookup"><span data-stu-id="d875f-125">If both are omitted, the contributor role is assigned to the service principal.</span></span> <span data-ttu-id="d875f-126">По умолчанию для параметров **"Роль"** и **"Область"** **заданы значения "Участник"** для текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="d875f-126">The default values for the **Role** and **Scope** parameters are **Contributor** for the current subscription.</span></span> <span data-ttu-id="d875f-127">Он создает приложение и задает его свойства, если он не предоставлен.</span><span class="sxs-lookup"><span data-stu-id="d875f-127">The cmdlet creates an application and sets its properties if an ApplicationId is not provided.</span></span> <span data-ttu-id="d875f-128">Чтобы обновить параметры конкретного приложения, используйте [cmdlet Update-AzADApplication.](./update-azadapplication.md)</span><span class="sxs-lookup"><span data-stu-id="d875f-128">To update the application-specific parameters, use the [Update-AzADApplication](./update-azadapplication.md) cmdlet.</span></span>

> [!WARNING]
> <span data-ttu-id="d875f-129">Когда вы создаете главную службу с помощью команды **New-AzADServicePrincipal,** выходные данные включают учетные данные, которые необходимо защитить.</span><span class="sxs-lookup"><span data-stu-id="d875f-129">When you create a service principal using the **New-AzADServicePrincipal** command, the output includes credentials that you must protect.</span></span> <span data-ttu-id="d875f-130">Не включите эти учетные данные в код и не проверяйте их в источнике данных.</span><span class="sxs-lookup"><span data-stu-id="d875f-130">Be sure that you do not include these credentials in your code or check the credentials into your source control.</span></span> <span data-ttu-id="d875f-131">В качестве альтернативы можно использовать [управляемые удостоверения,](/azure/active-directory/managed-identities-azure-resources/overview) чтобы избежать необходимости использовать учетные данные.</span><span class="sxs-lookup"><span data-stu-id="d875f-131">As an alternative, consider using [managed identities](/azure/active-directory/managed-identities-azure-resources/overview) to avoid the need to use credentials.</span></span>
>
> <span data-ttu-id="d875f-132">По умолчанию **New-AzADServicePrincipal** назначает [](/azure/role-based-access-control/built-in-roles#contributor) роль Участника основной службе в области подписки.</span><span class="sxs-lookup"><span data-stu-id="d875f-132">By default, **New-AzADServicePrincipal** assigns the [Contributor](/azure/role-based-access-control/built-in-roles#contributor) role to the service principal at the subscription scope.</span></span> <span data-ttu-id="d875f-133">Чтобы снизить риск компрометации основной службы, назначьте более определенную роль и сузьте область действия до группы ресурсов или ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d875f-133">To reduce your risk of a compromised service principal, assign a more specific role and narrow the scope to a resource or resource group.</span></span> <span data-ttu-id="d875f-134">Дополнительные [сведения см. в сведениях](/azure/role-based-access-control/role-assignments-steps) о добавлении назначения роли в этой области.</span><span class="sxs-lookup"><span data-stu-id="d875f-134">See [Steps to add a role assignment](/azure/role-based-access-control/role-assignments-steps) for more information.</span></span>

## <span data-ttu-id="d875f-135">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d875f-135">EXAMPLES</span></span>

### <span data-ttu-id="d875f-136">Пример 1. Простое создание главной службы AD</span><span class="sxs-lookup"><span data-stu-id="d875f-136">Example 1: Simple AD service principal creation</span></span>

<span data-ttu-id="d875f-137">В следующем примере создается principal-служба AD с использованием значений по умолчанию для параметров, не указанных.</span><span class="sxs-lookup"><span data-stu-id="d875f-137">The following example creates an AD service principal using default values for parameters not specified.</span></span> <span data-ttu-id="d875f-138">Так как не предоставлен ИД приложения, для директора-службы создается приложение.</span><span class="sxs-lookup"><span data-stu-id="d875f-138">Since an application ID is not provided, an application is created for the service principal.</span></span> <span data-ttu-id="d875f-139">Так как для роли  или области не запредоставляются **значения,** созданному участнику службы назначена роль участника для текущей подписки. </span><span class="sxs-lookup"><span data-stu-id="d875f-139">Since no values are provided for **Role** or **Scope**, the created service principal is assigned the **contributor** role for the current subscription.</span></span>

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

### <span data-ttu-id="d875f-140">Пример 2. Простое создание основной службы AD с указанной ролью и областью по умолчанию</span><span class="sxs-lookup"><span data-stu-id="d875f-140">Example 2: Simple AD service principal creation with a specified role and default scope</span></span>

<span data-ttu-id="d875f-141">В следующем примере создается principal-служба AD с использованием значений по умолчанию для параметров, не указанных.</span><span class="sxs-lookup"><span data-stu-id="d875f-141">The following example creates an AD service principal using the default values for parameters not specified.</span></span> <span data-ttu-id="d875f-142">Так как он не предоставлен, для основного обслуживания создается приложение.</span><span class="sxs-lookup"><span data-stu-id="d875f-142">Since the application ID is not provided, an application is created for the service principal.</span></span> <span data-ttu-id="d875f-143">Principal service principal is created with **Reader** permissions for the current subscription since no value is provided for the **Scope** parameter.</span><span class="sxs-lookup"><span data-stu-id="d875f-143">The service principal is created with **Reader** permissions for the current subscription since no value is provided for the **Scope** parameter.</span></span>

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

### <span data-ttu-id="d875f-144">Пример 3. Простое создание основной службы AD с заданной областью и ролью по умолчанию</span><span class="sxs-lookup"><span data-stu-id="d875f-144">Example 3: Simple AD service principal creation with a specified scope and default role</span></span>

<span data-ttu-id="d875f-145">В следующем примере создается principal-служба AD с использованием значений по умолчанию для параметров, не указанных.</span><span class="sxs-lookup"><span data-stu-id="d875f-145">The following example creates an AD service principal using the default values for parameters not specified.</span></span> <span data-ttu-id="d875f-146">Так как он не предоставлен, для основного обслуживания создается приложение.</span><span class="sxs-lookup"><span data-stu-id="d875f-146">Since the application ID is not provided, an application is created for the service principal.</span></span> <span data-ttu-id="d875f-147">Для участника-службы создаются разрешения **участника** для заданной области группы ресурсов, так как для параметра **Role** не задано значение.</span><span class="sxs-lookup"><span data-stu-id="d875f-147">The service principal is created with **Contributor** permissions for the provided resource group scope since no value is provided for the **Role** parameter.</span></span>

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

### <span data-ttu-id="d875f-148">Пример 4. Простое создание основной службы AD с заданной областью и ролью</span><span class="sxs-lookup"><span data-stu-id="d875f-148">Example 4: Simple AD service principal creation with a specified scope and role</span></span>

<span data-ttu-id="d875f-149">В следующем примере создается principal-служба AD с использованием значений по умолчанию для параметров, не указанных.</span><span class="sxs-lookup"><span data-stu-id="d875f-149">The following example creates an AD service principal using the default values for parameters not specified.</span></span> <span data-ttu-id="d875f-150">Так как он не предоставлен, для основного обслуживания создается приложение.</span><span class="sxs-lookup"><span data-stu-id="d875f-150">Since the application ID is not provided, an application is created for the service principal.</span></span> <span data-ttu-id="d875f-151">При этом создается principal-служба **с** разрешениями на чтение для предоставляются области для группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d875f-151">The service principal is created with **Reader** permissions for the provided resource group scope.</span></span>

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

### <span data-ttu-id="d875f-152">Пример 5. Создание новой основной роли службы AD с помощью ИД приложения с назначением ролей</span><span class="sxs-lookup"><span data-stu-id="d875f-152">Example 5: Create a new AD service principal using application ID with role assignment</span></span>

<span data-ttu-id="d875f-153">В следующем примере для приложения создается новая главная служба AD с ИД приложения "00000000-0000-0000-0000-0000000000000".</span><span class="sxs-lookup"><span data-stu-id="d875f-153">The following example creates a new AD service principal for the application with application ID '00000000-0000-0000-0000-000000000000'.</span></span> <span data-ttu-id="d875f-154">Так как для роли  или области не запредоставляются **значения,** созданному участнику службы назначена роль участника для текущей подписки. </span><span class="sxs-lookup"><span data-stu-id="d875f-154">Since no values are provided for **Role** or **Scope**, the created service principal is assigned the **contributor** role for the current subscription.</span></span>

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

### <span data-ttu-id="d875f-155">Пример 6. Создание новой основной суммы службы AD с помощью piping</span><span class="sxs-lookup"><span data-stu-id="d875f-155">Example 6: Create a new AD service principal using piping</span></span>

<span data-ttu-id="d875f-156">В следующем примере приложение извлекает приложение с ИД объекта '3ede3c26-b443-4e0b-9efc-b05e68338dc3' с помощью [cmdlet Get-AzADApplication.](./get-azadapplication.md)</span><span class="sxs-lookup"><span data-stu-id="d875f-156">The following example retrieves the application with object ID '3ede3c26-b443-4e0b-9efc-b05e68338dc3' using the [Get-AzADApplication](./get-azadapplication.md) cmdlet.</span></span> <span data-ttu-id="d875f-157">Результаты перенакладыются в этот проект, чтобы создать для этого приложения новую `New-AzADServicePrincipal` главную службу AD.</span><span class="sxs-lookup"><span data-stu-id="d875f-157">The results are piped to the `New-AzADServicePrincipal` cmdlet to create a new AD service principal for that application.</span></span>

```powershell
Get-AzADApplication -ObjectId 3ede3c26-b443-4e0b-9efc-b05e68338dc3 | New-AzADServicePrincipal
```

### <span data-ttu-id="d875f-158">Пример 7. Создание новой основной службы AD с использованием DisplayName и учетных данных для пароля</span><span class="sxs-lookup"><span data-stu-id="d875f-158">Example 7: Create a new AD service principal using DisplayName and password credential</span></span>

<span data-ttu-id="d875f-159">В следующем примере создается новое приложение с именем **ServicePrincipalName и** паролем **StrongPassworld!23.**</span><span class="sxs-lookup"><span data-stu-id="d875f-159">The following example creates a new application with the name **ServicePrincipalName** and a password of **StrongPassworld!23**.</span></span> <span data-ttu-id="d875f-160">Она создает главную службу на основе созданного приложения.</span><span class="sxs-lookup"><span data-stu-id="d875f-160">It creates the service principal based on the created application.</span></span> <span data-ttu-id="d875f-161">К учетным данным пароля добавляются даты начала и окончания.</span><span class="sxs-lookup"><span data-stu-id="d875f-161">The start date and end date are added to the password credential.</span></span>

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

### <span data-ttu-id="d875f-162">Пример 8. Создание новой основной службы AD с использованием DisplayName и обычных учетных данных ключа</span><span class="sxs-lookup"><span data-stu-id="d875f-162">Example 8: Create a new AD service principal using DisplayName and plain key credential</span></span>

<span data-ttu-id="d875f-163">В следующем примере создается новое приложение с именем **ServicePrincipalName** **и сертификатом $cert.** Она создает главную службу на основе созданного приложения.</span><span class="sxs-lookup"><span data-stu-id="d875f-163">The following example creates a new application with the name **ServicePrincipalName** and a certificate **$cert**. It creates the service principal based on the application created.</span></span> <span data-ttu-id="d875f-164">Даты окончания добавляются к учетным данным ключа.</span><span class="sxs-lookup"><span data-stu-id="d875f-164">The end date is added to key credential.</span></span>

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

## <span data-ttu-id="d875f-165">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d875f-165">PARAMETERS</span></span>

### <span data-ttu-id="d875f-166">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="d875f-166">-ApplicationId</span></span>

<span data-ttu-id="d875f-167">Уникальный ИД приложения для основной службы в клиенте.</span><span class="sxs-lookup"><span data-stu-id="d875f-167">The unique application ID for a service principal in a tenant.</span></span> <span data-ttu-id="d875f-168">Созданное свойство невозможно изменить.</span><span class="sxs-lookup"><span data-stu-id="d875f-168">Once created this property cannot be changed.</span></span> <span data-ttu-id="d875f-169">Если в существующем приложении не указан ИД приложения, создается приложение.</span><span class="sxs-lookup"><span data-stu-id="d875f-169">If an application ID for an existing application is not specified, an application is created.</span></span>

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

### <span data-ttu-id="d875f-170">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="d875f-170">-ApplicationObject</span></span>

<span data-ttu-id="d875f-171">Объект, представляющий приложение, для которого создается основной службы.</span><span class="sxs-lookup"><span data-stu-id="d875f-171">The object representing the application for which the service principal is created.</span></span>

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

### <span data-ttu-id="d875f-172">-CertValue</span><span class="sxs-lookup"><span data-stu-id="d875f-172">-CertValue</span></span>

<span data-ttu-id="d875f-173">Значение асимметричного типа учетных данных.</span><span class="sxs-lookup"><span data-stu-id="d875f-173">The value of the asymmetric credential type.</span></span> <span data-ttu-id="d875f-174">Он представляет зашифрованный сертификат Base64.</span><span class="sxs-lookup"><span data-stu-id="d875f-174">It represents the Base64 encoded certificate.</span></span>

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

### <span data-ttu-id="d875f-175">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d875f-175">-DefaultProfile</span></span>

<span data-ttu-id="d875f-176">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d875f-176">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d875f-177">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="d875f-177">-DisplayName</span></span>

<span data-ttu-id="d875f-178">Удобное имя директора-службы.</span><span class="sxs-lookup"><span data-stu-id="d875f-178">The friendly name of the service principal.</span></span> <span data-ttu-id="d875f-179">Если отображаемого имени нет, по умолчанию для этого значения задается **azure-powershell-MM-dd-y-HH-mm-ss,** где суффикс — время создания приложения.</span><span class="sxs-lookup"><span data-stu-id="d875f-179">If a display name is not provided, this value will default to **azure-powershell-MM-dd-yyyy-HH-mm-ss** where the suffix is the time of application creation.</span></span>

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

### <span data-ttu-id="d875f-180">-EndDate</span><span class="sxs-lookup"><span data-stu-id="d875f-180">-EndDate</span></span>

<span data-ttu-id="d875f-181">Дата окончания использования учетных данных.</span><span class="sxs-lookup"><span data-stu-id="d875f-181">The effective end date of the credential usage.</span></span> <span data-ttu-id="d875f-182">Значение даты окончания по умолчанию составляет один год от сегодняшнего дня.</span><span class="sxs-lookup"><span data-stu-id="d875f-182">The default end date value is one year from today.</span></span>
<span data-ttu-id="d875f-183">Для учетных данных асимметричного типа это должно быть установлено в день, когда действительный сертификат X509, или до нее.</span><span class="sxs-lookup"><span data-stu-id="d875f-183">For an asymmetric type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="d875f-184">-KeyCredential</span><span class="sxs-lookup"><span data-stu-id="d875f-184">-KeyCredential</span></span>

<span data-ttu-id="d875f-185">Набор учетных данных ключа, связанных с приложением.</span><span class="sxs-lookup"><span data-stu-id="d875f-185">The collection of key credentials associated with the application.</span></span>

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

### <span data-ttu-id="d875f-186">-PasswordCredential</span><span class="sxs-lookup"><span data-stu-id="d875f-186">-PasswordCredential</span></span>

<span data-ttu-id="d875f-187">Набор учетных данных, связанных с приложением.</span><span class="sxs-lookup"><span data-stu-id="d875f-187">The collection of password credentials associated with the application.</span></span>

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

### <span data-ttu-id="d875f-188">-Роль</span><span class="sxs-lookup"><span data-stu-id="d875f-188">-Role</span></span>

<span data-ttu-id="d875f-189">Роль, которая является основной службой, в рамках этой области.</span><span class="sxs-lookup"><span data-stu-id="d875f-189">The role that the service principal has over the scope.</span></span> <span data-ttu-id="d875f-190">Если значение не за предоставлено, **для роли** "Участник" по умолчанию запредоставляются **роли "Участник".**</span><span class="sxs-lookup"><span data-stu-id="d875f-190">If no value is provided, **Role** defaults to the **Contributor** role.</span></span>

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

### <span data-ttu-id="d875f-191">-Scope</span><span class="sxs-lookup"><span data-stu-id="d875f-191">-Scope</span></span>

<span data-ttu-id="d875f-192">Область, на которую у директора-службы есть разрешения.</span><span class="sxs-lookup"><span data-stu-id="d875f-192">The scope that the service principal has permissions for.</span></span> <span data-ttu-id="d875f-193">Если значение не  за предоставлено, по умолчанию за работой по области действия будет за ценные суммы для текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="d875f-193">If no value is provided, **Scope** defaults to the current subscription.</span></span>

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

### <span data-ttu-id="d875f-194">-SkipAssignment</span><span class="sxs-lookup"><span data-stu-id="d875f-194">-SkipAssignment</span></span>

<span data-ttu-id="d875f-195">Если за установлено, пропустите создание назначения роли по умолчанию для основного задания службы.</span><span class="sxs-lookup"><span data-stu-id="d875f-195">If set, skip creating the default role assignment for the service principal.</span></span>

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

### <span data-ttu-id="d875f-196">-StartDate</span><span class="sxs-lookup"><span data-stu-id="d875f-196">-StartDate</span></span>

<span data-ttu-id="d875f-197">Начальную дату использования учетных данных.</span><span class="sxs-lookup"><span data-stu-id="d875f-197">The effective start date of the credential usage.</span></span> <span data-ttu-id="d875f-198">По умолчанию дата начала является сегодняшним значением.</span><span class="sxs-lookup"><span data-stu-id="d875f-198">The default start date value is today.</span></span> <span data-ttu-id="d875f-199">Для учетных данных асимметричного типа это должно быть установлено в дату, начиная с даты действия сертификата X509, или после нее.</span><span class="sxs-lookup"><span data-stu-id="d875f-199">For an asymmetric type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="d875f-200">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d875f-200">-Confirm</span></span>

<span data-ttu-id="d875f-201">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="d875f-201">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d875f-202">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d875f-202">-WhatIf</span></span>

<span data-ttu-id="d875f-203">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d875f-203">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d875f-204">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d875f-204">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d875f-205">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d875f-205">CommonParameters</span></span>
<span data-ttu-id="d875f-206">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d875f-206">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d875f-207">Дополнительные сведения см. [в about_CommonParameters.](/powershell/module/microsoft.powershell.core/about/about_commonparameters)</span><span class="sxs-lookup"><span data-stu-id="d875f-207">For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span></span>
## <span data-ttu-id="d875f-208">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d875f-208">INPUTS</span></span>

### <span data-ttu-id="d875f-209">System.Guid</span><span class="sxs-lookup"><span data-stu-id="d875f-209">System.Guid</span></span>

### <span data-ttu-id="d875f-210">System.String</span><span class="sxs-lookup"><span data-stu-id="d875f-210">System.String</span></span>

### <span data-ttu-id="d875f-211">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="d875f-211">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

### <span data-ttu-id="d875f-212">Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]</span><span class="sxs-lookup"><span data-stu-id="d875f-212">Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]</span></span>

### <span data-ttu-id="d875f-213">Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]</span><span class="sxs-lookup"><span data-stu-id="d875f-213">Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]</span></span>

### <span data-ttu-id="d875f-214">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="d875f-214">System.DateTime</span></span>

## <span data-ttu-id="d875f-215">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d875f-215">OUTPUTS</span></span>

### <span data-ttu-id="d875f-216">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="d875f-216">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="d875f-217">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADServicePrincipalWrapper</span><span class="sxs-lookup"><span data-stu-id="d875f-217">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADServicePrincipalWrapper</span></span>

## <span data-ttu-id="d875f-218">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d875f-218">NOTES</span></span>

<span data-ttu-id="d875f-219">Ключевые слова: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span><span class="sxs-lookup"><span data-stu-id="d875f-219">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="d875f-220">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d875f-220">RELATED LINKS</span></span>

[<span data-ttu-id="d875f-221">Remove-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="d875f-221">Remove-AzADServicePrincipal</span></span>](./Remove-AzADServicePrincipal.md)

[<span data-ttu-id="d875f-222">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="d875f-222">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

[<span data-ttu-id="d875f-223">New-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="d875f-223">New-AzADApplication</span></span>](./New-AzADApplication.md)

[<span data-ttu-id="d875f-224">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="d875f-224">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="d875f-225">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="d875f-225">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

[<span data-ttu-id="d875f-226">New-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="d875f-226">New-AzADSpCredential</span></span>](./New-AzADSpCredential.md)

[<span data-ttu-id="d875f-227">Remove-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="d875f-227">Remove-AzADSpCredential</span></span>](./Remove-AzADSpCredential.md)