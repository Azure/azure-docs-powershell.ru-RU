---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D602F910-B26F-473D-B5B6-C7BDFB0A14CB
online version: https://docs.microsoft.com/powershell/module/az.resources/new-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
ms.openlocfilehash: f826ecbde81bc301cc51e031b2047bc7a9f284e1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988924"
---
# <span data-ttu-id="ea88e-101">New-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="ea88e-101">New-AzADServicePrincipal</span></span>

## <span data-ttu-id="ea88e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea88e-102">SYNOPSIS</span></span>
<span data-ttu-id="ea88e-103">Создает новую главную службу Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ea88e-103">Creates a new Azure active directory service principal.</span></span>

## <span data-ttu-id="ea88e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ea88e-104">SYNTAX</span></span>

### <span data-ttu-id="ea88e-105">SimpleParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ea88e-105">SimpleParameterSet (Default)</span></span>

```
New-AzADServicePrincipal [-ApplicationId <Guid>] [-DisplayName <String>] [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-Scope <String>] [-Role <String>] [-SkipAssignment]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea88e-106">ApplicationWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea88e-106">ApplicationWithoutCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ea88e-107">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea88e-107">ApplicationWithPasswordPlainParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationId <Guid> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea88e-108">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea88e-108">ApplicationWithPasswordCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationId <Guid> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea88e-109">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea88e-109">ApplicationWithKeyPlainParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationId <Guid> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea88e-110">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea88e-110">ApplicationWithKeyCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationId <Guid> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea88e-111">DisplayNameWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea88e-111">DisplayNameWithoutCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ea88e-112">DisplayNameWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea88e-112">DisplayNameWithPasswordPlainParameterSet</span></span>

```
New-AzADServicePrincipal -DisplayName <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea88e-113">DisplayNameWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea88e-113">DisplayNameWithPasswordCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -DisplayName <String> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea88e-114">DisplayNameWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea88e-114">DisplayNameWithKeyPlainParameterSet</span></span>

```
New-AzADServicePrincipal -DisplayName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea88e-115">DisplayNameWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea88e-115">DisplayNameWithKeyCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -DisplayName <String> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea88e-116">ApplicationObjectWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea88e-116">ApplicationObjectWithPasswordPlainParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea88e-117">ApplicationObjectWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea88e-117">ApplicationObjectWithPasswordCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea88e-118">ApplicationObjectWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea88e-118">ApplicationObjectWithKeyPlainParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea88e-119">ApplicationObjectWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea88e-119">ApplicationObjectWithKeyCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea88e-120">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ea88e-120">DESCRIPTION</span></span>

<span data-ttu-id="ea88e-121">Создает новую главную службу Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ea88e-121">Creates a new Azure active directory service principal.</span></span> <span data-ttu-id="ea88e-122">В наборе параметров по умолчанию используются значения по умолчанию для параметров, если они не заданы.</span><span class="sxs-lookup"><span data-stu-id="ea88e-122">The default parameter set uses default values for parameters if they are not provided.</span></span> <span data-ttu-id="ea88e-123">Дополнительные сведения о значениях по умолчанию см. в описании каждого параметра.</span><span class="sxs-lookup"><span data-stu-id="ea88e-123">For more information on default values, see the description for each parameter.</span></span> <span data-ttu-id="ea88e-124">С помощью этого cmdlet можно назначить роль главе службы с параметрами **"Роль"** и **"Область".**</span><span class="sxs-lookup"><span data-stu-id="ea88e-124">This cmdlet has the ability to assign a role to the service principal with the **Role** and **Scope** parameters.</span></span> <span data-ttu-id="ea88e-125">Если обе функции опущены, роль участника назначена участнику службы.</span><span class="sxs-lookup"><span data-stu-id="ea88e-125">If both are omitted, the contributor role is assigned to the service principal.</span></span> <span data-ttu-id="ea88e-126">По умолчанию для параметров **"Роль"** и **"Область"** **заданы значения "Участник"** для текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="ea88e-126">The default values for the **Role** and **Scope** parameters are **Contributor** for the current subscription.</span></span> <span data-ttu-id="ea88e-127">Он создает приложение и задает его свойства, если он не предоставлен.</span><span class="sxs-lookup"><span data-stu-id="ea88e-127">The cmdlet creates an application and sets its properties if an ApplicationId is not provided.</span></span> <span data-ttu-id="ea88e-128">Чтобы обновить параметры конкретного приложения, используйте [cmdlet Update-AzADApplication.](./update-azadapplication.md)</span><span class="sxs-lookup"><span data-stu-id="ea88e-128">To update the application-specific parameters, use the [Update-AzADApplication](./update-azadapplication.md) cmdlet.</span></span>

> [!WARNING]
> <span data-ttu-id="ea88e-129">Когда вы создаете главную службу с помощью команды **New-AzADServicePrincipal,** выходные данные включают учетные данные, которые необходимо защитить.</span><span class="sxs-lookup"><span data-stu-id="ea88e-129">When you create a service principal using the **New-AzADServicePrincipal** command, the output includes credentials that you must protect.</span></span> <span data-ttu-id="ea88e-130">В качестве альтернативы можно использовать [управляемые удостоверения,](/azure/active-directory/managed-identities-azure-resources/overview) чтобы избежать необходимости использовать учетные данные.</span><span class="sxs-lookup"><span data-stu-id="ea88e-130">As an alternative, consider using [managed identities](/azure/active-directory/managed-identities-azure-resources/overview) to avoid the need to use credentials.</span></span>
>
> <span data-ttu-id="ea88e-131">По умолчанию **New-AzADServicePrincipal** назначает [](/azure/role-based-access-control/built-in-roles#contributor) роль Участника основной службе в области подписки.</span><span class="sxs-lookup"><span data-stu-id="ea88e-131">By default, **New-AzADServicePrincipal** assigns the [Contributor](/azure/role-based-access-control/built-in-roles#contributor) role to the service principal at the subscription scope.</span></span> <span data-ttu-id="ea88e-132">Чтобы снизить риск компрометации основной службы, назначьте более определенную роль и сузьте область действия до группы ресурсов или ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ea88e-132">To reduce your risk of a compromised service principal, assign a more specific role and narrow the scope to a resource or resource group.</span></span> <span data-ttu-id="ea88e-133">Дополнительные [сведения см. в сведениях](/azure/role-based-access-control/role-assignments-steps) о добавлении назначения роли в этой области.</span><span class="sxs-lookup"><span data-stu-id="ea88e-133">See [Steps to add a role assignment](/azure/role-based-access-control/role-assignments-steps) for more information.</span></span>

## <span data-ttu-id="ea88e-134">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ea88e-134">EXAMPLES</span></span>

### <span data-ttu-id="ea88e-135">Пример 1. Простое создание основной службы AD</span><span class="sxs-lookup"><span data-stu-id="ea88e-135">Example 1: Simple AD service principal creation</span></span>

<span data-ttu-id="ea88e-136">В следующем примере создается principal-служба AD с использованием значений по умолчанию для параметров, не указанных.</span><span class="sxs-lookup"><span data-stu-id="ea88e-136">The following example creates an AD service principal using default values for parameters not specified.</span></span> <span data-ttu-id="ea88e-137">Так как не предоставлен ИД приложения, для директора-службы создается приложение.</span><span class="sxs-lookup"><span data-stu-id="ea88e-137">Since an application ID is not provided, an application is created for the service principal.</span></span> <span data-ttu-id="ea88e-138">Поскольку для роли или  области не предоставлены **значения,** созданной основной службе назначена роль участника для текущей подписки. </span><span class="sxs-lookup"><span data-stu-id="ea88e-138">Since no values are provided for **Role** or **Scope**, the created service principal is assigned the **contributor** role for the current subscription.</span></span>

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

### <span data-ttu-id="ea88e-139">Пример 2. Простое создание основной службы AD с заданной ролью и областью по умолчанию</span><span class="sxs-lookup"><span data-stu-id="ea88e-139">Example 2: Simple AD service principal creation with a specified role and default scope</span></span>

<span data-ttu-id="ea88e-140">В следующем примере создается principal-служба AD с использованием значений по умолчанию для параметров, не указанных.</span><span class="sxs-lookup"><span data-stu-id="ea88e-140">The following example creates an AD service principal using the default values for parameters not specified.</span></span> <span data-ttu-id="ea88e-141">Так как он не предоставлен, для основного обслуживания создается приложение.</span><span class="sxs-lookup"><span data-stu-id="ea88e-141">Since the application ID is not provided, an application is created for the service principal.</span></span> <span data-ttu-id="ea88e-142">Principal service principal is created with **Reader** permissions for the current subscription since no value is provided for the **Scope** parameter.</span><span class="sxs-lookup"><span data-stu-id="ea88e-142">The service principal is created with **Reader** permissions for the current subscription since no value is provided for the **Scope** parameter.</span></span>

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

### <span data-ttu-id="ea88e-143">Пример 3. Простое создание основной службы AD с заданной областью и ролью по умолчанию</span><span class="sxs-lookup"><span data-stu-id="ea88e-143">Example 3: Simple AD service principal creation with a specified scope and default role</span></span>

<span data-ttu-id="ea88e-144">В следующем примере создается principal-служба AD с использованием значений по умолчанию для параметров, не указанных.</span><span class="sxs-lookup"><span data-stu-id="ea88e-144">The following example creates an AD service principal using the default values for parameters not specified.</span></span> <span data-ttu-id="ea88e-145">Так как он не предоставлен, для основного обслуживания создается приложение.</span><span class="sxs-lookup"><span data-stu-id="ea88e-145">Since the application ID is not provided, an application is created for the service principal.</span></span> <span data-ttu-id="ea88e-146">Для участника-службы создаются разрешения **участника** для заданной области группы ресурсов, так как для параметра **Role** не задано значение.</span><span class="sxs-lookup"><span data-stu-id="ea88e-146">The service principal is created with **Contributor** permissions for the provided resource group scope since no value is provided for the **Role** parameter.</span></span>

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

### <span data-ttu-id="ea88e-147">Пример 4. Простое создание основной службы AD с заданной областью и ролью</span><span class="sxs-lookup"><span data-stu-id="ea88e-147">Example 4: Simple AD service principal creation with a specified scope and role</span></span>

<span data-ttu-id="ea88e-148">В следующем примере создается principal-служба AD с использованием значений по умолчанию для параметров, не указанных.</span><span class="sxs-lookup"><span data-stu-id="ea88e-148">The following example creates an AD service principal using the default values for parameters not specified.</span></span> <span data-ttu-id="ea88e-149">Так как он не предоставлен, для основного обслуживания создается приложение.</span><span class="sxs-lookup"><span data-stu-id="ea88e-149">Since the application ID is not provided, an application is created for the service principal.</span></span> <span data-ttu-id="ea88e-150">При этом создается principal-служба **с** разрешениями на чтение для предоставляются области для группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ea88e-150">The service principal is created with **Reader** permissions for the provided resource group scope.</span></span>

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

### <span data-ttu-id="ea88e-151">Пример 5. Создание новой основной роли службы AD с помощью ИД приложения с назначением ролей</span><span class="sxs-lookup"><span data-stu-id="ea88e-151">Example 5: Create a new AD service principal using application ID with role assignment</span></span>

<span data-ttu-id="ea88e-152">В следующем примере для приложения создается новая главная служба AD с ИД приложения "00000000-0000-0000-0000-0000000000000".</span><span class="sxs-lookup"><span data-stu-id="ea88e-152">The following example creates a new AD service principal for the application with application ID '00000000-0000-0000-0000-000000000000'.</span></span> <span data-ttu-id="ea88e-153">Поскольку для роли или  области не предоставлены **значения,** созданной основной службе назначена роль участника для текущей подписки. </span><span class="sxs-lookup"><span data-stu-id="ea88e-153">Since no values are provided for **Role** or **Scope**, the created service principal is assigned the **contributor** role for the current subscription.</span></span>

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

### <span data-ttu-id="ea88e-154">Пример 6. Создание новой основной суммы службы AD с помощью piping</span><span class="sxs-lookup"><span data-stu-id="ea88e-154">Example 6: Create a new AD service principal using piping</span></span>

<span data-ttu-id="ea88e-155">В следующем примере приложение извлекает приложение с ИД объекта '3ede3c26-b443-4e0b-9efc-b05e68338dc3' с помощью [cmdlet Get-AzADApplication.](./get-azadapplication.md)</span><span class="sxs-lookup"><span data-stu-id="ea88e-155">The following example retrieves the application with object ID '3ede3c26-b443-4e0b-9efc-b05e68338dc3' using the [Get-AzADApplication](./get-azadapplication.md) cmdlet.</span></span> <span data-ttu-id="ea88e-156">Результаты перенакладыются в этот cmdlet, чтобы создать для этого приложения новую `New-AzADServicePrincipal` главную службу AD.</span><span class="sxs-lookup"><span data-stu-id="ea88e-156">The results are piped to the `New-AzADServicePrincipal` cmdlet to create a new AD service principal for that application.</span></span>

```powershell
Get-AzADApplication -ObjectId 3ede3c26-b443-4e0b-9efc-b05e68338dc3 | New-AzADServicePrincipal
```

### <span data-ttu-id="ea88e-157">Пример 7. Создание новой основной службы AD с использованием DisplayName и учетных данных для пароля</span><span class="sxs-lookup"><span data-stu-id="ea88e-157">Example 7: Create a new AD service principal using DisplayName and password credential</span></span>

<span data-ttu-id="ea88e-158">В следующем примере создается новое приложение с именем **ServicePrincipalName и** паролем **StrongPassworld!23.**</span><span class="sxs-lookup"><span data-stu-id="ea88e-158">The following example creates a new application with the name **ServicePrincipalName** and a password of **StrongPassworld!23**.</span></span> <span data-ttu-id="ea88e-159">Она создает главную службу на основе созданного приложения.</span><span class="sxs-lookup"><span data-stu-id="ea88e-159">It creates the service principal based on the created application.</span></span> <span data-ttu-id="ea88e-160">К учетным данным пароля добавляются даты начала и окончания.</span><span class="sxs-lookup"><span data-stu-id="ea88e-160">The start date and end date are added to the password credential.</span></span>

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

### <span data-ttu-id="ea88e-161">Пример 8. Создание новой основной службы AD с использованием DisplayName и обычных учетных данных ключа</span><span class="sxs-lookup"><span data-stu-id="ea88e-161">Example 8: Create a new AD service principal using DisplayName and plain key credential</span></span>

<span data-ttu-id="ea88e-162">В следующем примере создается новое приложение с именем **ServicePrincipalName** **и сертификатом $cert.** Она создает главную службу на основе созданного приложения.</span><span class="sxs-lookup"><span data-stu-id="ea88e-162">The following example creates a new application with the name **ServicePrincipalName** and a certificate **$cert**. It creates the service principal based on the application created.</span></span> <span data-ttu-id="ea88e-163">Даты окончания добавляются к учетным данным ключа.</span><span class="sxs-lookup"><span data-stu-id="ea88e-163">The end date is added to key credential.</span></span>

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

## <span data-ttu-id="ea88e-164">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ea88e-164">PARAMETERS</span></span>

### <span data-ttu-id="ea88e-165">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="ea88e-165">-ApplicationId</span></span>

<span data-ttu-id="ea88e-166">Уникальный ИД приложения для основной службы в клиенте.</span><span class="sxs-lookup"><span data-stu-id="ea88e-166">The unique application ID for a service principal in a tenant.</span></span> <span data-ttu-id="ea88e-167">Созданное свойство невозможно изменить.</span><span class="sxs-lookup"><span data-stu-id="ea88e-167">Once created this property cannot be changed.</span></span> <span data-ttu-id="ea88e-168">Если в существующем приложении не указан ИД приложения, создается приложение.</span><span class="sxs-lookup"><span data-stu-id="ea88e-168">If an application ID for an existing application is not specified, an application is created.</span></span>

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

### <span data-ttu-id="ea88e-169">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="ea88e-169">-ApplicationObject</span></span>

<span data-ttu-id="ea88e-170">Объект, представляющий приложение, для которого создается основной службы.</span><span class="sxs-lookup"><span data-stu-id="ea88e-170">The object representing the application for which the service principal is created.</span></span>

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

### <span data-ttu-id="ea88e-171">-CertValue</span><span class="sxs-lookup"><span data-stu-id="ea88e-171">-CertValue</span></span>

<span data-ttu-id="ea88e-172">Значение асимметричного типа учетных данных.</span><span class="sxs-lookup"><span data-stu-id="ea88e-172">The value of the asymmetric credential type.</span></span> <span data-ttu-id="ea88e-173">Он представляет зашифрованный сертификат Base64.</span><span class="sxs-lookup"><span data-stu-id="ea88e-173">It represents the Base64 encoded certificate.</span></span>

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

### <span data-ttu-id="ea88e-174">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea88e-174">-DefaultProfile</span></span>

<span data-ttu-id="ea88e-175">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ea88e-175">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea88e-176">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="ea88e-176">-DisplayName</span></span>

<span data-ttu-id="ea88e-177">Удобное имя директора-службы.</span><span class="sxs-lookup"><span data-stu-id="ea88e-177">The friendly name of the service principal.</span></span> <span data-ttu-id="ea88e-178">Если отображаемого имени нет, по умолчанию для этого значения задается **azure-powershell-MM-dd-yyyy-HH-mm-ss,** где суффикс — время создания приложения.</span><span class="sxs-lookup"><span data-stu-id="ea88e-178">If a display name is not provided, this value will default to **azure-powershell-MM-dd-yyyy-HH-mm-ss** where the suffix is the time of application creation.</span></span>

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

### <span data-ttu-id="ea88e-179">-EndDate</span><span class="sxs-lookup"><span data-stu-id="ea88e-179">-EndDate</span></span>

<span data-ttu-id="ea88e-180">Дата окончания использования учетных данных.</span><span class="sxs-lookup"><span data-stu-id="ea88e-180">The effective end date of the credential usage.</span></span> <span data-ttu-id="ea88e-181">Значение даты окончания по умолчанию составляет один год от сегодняшнего дня.</span><span class="sxs-lookup"><span data-stu-id="ea88e-181">The default end date value is one year from today.</span></span>
<span data-ttu-id="ea88e-182">Для учетных данных асимметричного типа это должно быть установлено в день, когда допустим сертификат X509 или раньше нее.</span><span class="sxs-lookup"><span data-stu-id="ea88e-182">For an asymmetric type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="ea88e-183">-KeyCredential</span><span class="sxs-lookup"><span data-stu-id="ea88e-183">-KeyCredential</span></span>

<span data-ttu-id="ea88e-184">Набор учетных данных ключа, связанных с приложением.</span><span class="sxs-lookup"><span data-stu-id="ea88e-184">The collection of key credentials associated with the application.</span></span>

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

### <span data-ttu-id="ea88e-185">-PasswordCredential</span><span class="sxs-lookup"><span data-stu-id="ea88e-185">-PasswordCredential</span></span>

<span data-ttu-id="ea88e-186">Набор учетных данных, связанных с приложением.</span><span class="sxs-lookup"><span data-stu-id="ea88e-186">The collection of password credentials associated with the application.</span></span>

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

### <span data-ttu-id="ea88e-187">-Роль</span><span class="sxs-lookup"><span data-stu-id="ea88e-187">-Role</span></span>

<span data-ttu-id="ea88e-188">Роль, которая является основной службой в рамках этой области.</span><span class="sxs-lookup"><span data-stu-id="ea88e-188">The role that the service principal has over the scope.</span></span> <span data-ttu-id="ea88e-189">Если значение не за предоставлено, **для роли** "Участник" по умолчанию запредоставляются **роли "Участник".**</span><span class="sxs-lookup"><span data-stu-id="ea88e-189">If no value is provided, **Role** defaults to the **Contributor** role.</span></span>

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

### <span data-ttu-id="ea88e-190">-Scope</span><span class="sxs-lookup"><span data-stu-id="ea88e-190">-Scope</span></span>

<span data-ttu-id="ea88e-191">Область, на которую у директора-службы есть разрешения.</span><span class="sxs-lookup"><span data-stu-id="ea88e-191">The scope that the service principal has permissions for.</span></span> <span data-ttu-id="ea88e-192">Если значение не  за предоставлено, по умолчанию за работой по области действия будет за ценные суммы для текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="ea88e-192">If no value is provided, **Scope** defaults to the current subscription.</span></span>

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

### <span data-ttu-id="ea88e-193">-SkipAssignment</span><span class="sxs-lookup"><span data-stu-id="ea88e-193">-SkipAssignment</span></span>

<span data-ttu-id="ea88e-194">Если за установлено, пропустите создание назначения роли по умолчанию для основного задания службы.</span><span class="sxs-lookup"><span data-stu-id="ea88e-194">If set, skip creating the default role assignment for the service principal.</span></span>

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

### <span data-ttu-id="ea88e-195">-StartDate</span><span class="sxs-lookup"><span data-stu-id="ea88e-195">-StartDate</span></span>

<span data-ttu-id="ea88e-196">Начальную дату использования учетных данных.</span><span class="sxs-lookup"><span data-stu-id="ea88e-196">The effective start date of the credential usage.</span></span> <span data-ttu-id="ea88e-197">По умолчанию дата начала является сегодняшним значением.</span><span class="sxs-lookup"><span data-stu-id="ea88e-197">The default start date value is today.</span></span> <span data-ttu-id="ea88e-198">Для учетных данных асимметричного типа это должно быть установлено в дату, начиная с даты действия сертификата X509, или после нее.</span><span class="sxs-lookup"><span data-stu-id="ea88e-198">For an asymmetric type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="ea88e-199">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ea88e-199">-Confirm</span></span>

<span data-ttu-id="ea88e-200">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea88e-200">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea88e-201">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea88e-201">-WhatIf</span></span>

<span data-ttu-id="ea88e-202">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea88e-202">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ea88e-203">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ea88e-203">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea88e-204">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea88e-204">CommonParameters</span></span>
<span data-ttu-id="ea88e-205">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea88e-205">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea88e-206">Дополнительные сведения см. [в about_CommonParameters.](/powershell/module/microsoft.powershell.core/about/about_commonparameters)</span><span class="sxs-lookup"><span data-stu-id="ea88e-206">For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span></span>
## <span data-ttu-id="ea88e-207">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ea88e-207">INPUTS</span></span>

### <span data-ttu-id="ea88e-208">System.Guid</span><span class="sxs-lookup"><span data-stu-id="ea88e-208">System.Guid</span></span>

### <span data-ttu-id="ea88e-209">System.String</span><span class="sxs-lookup"><span data-stu-id="ea88e-209">System.String</span></span>

### <span data-ttu-id="ea88e-210">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="ea88e-210">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

### <span data-ttu-id="ea88e-211">Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]</span><span class="sxs-lookup"><span data-stu-id="ea88e-211">Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]</span></span>

### <span data-ttu-id="ea88e-212">Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]</span><span class="sxs-lookup"><span data-stu-id="ea88e-212">Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]</span></span>

### <span data-ttu-id="ea88e-213">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="ea88e-213">System.DateTime</span></span>

## <span data-ttu-id="ea88e-214">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ea88e-214">OUTPUTS</span></span>

### <span data-ttu-id="ea88e-215">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="ea88e-215">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="ea88e-216">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADServicePrincipalWrapper</span><span class="sxs-lookup"><span data-stu-id="ea88e-216">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADServicePrincipalWrapper</span></span>

## <span data-ttu-id="ea88e-217">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ea88e-217">NOTES</span></span>

<span data-ttu-id="ea88e-218">Ключевые слова: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span><span class="sxs-lookup"><span data-stu-id="ea88e-218">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="ea88e-219">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ea88e-219">RELATED LINKS</span></span>

[<span data-ttu-id="ea88e-220">Remove-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="ea88e-220">Remove-AzADServicePrincipal</span></span>](./Remove-AzADServicePrincipal.md)

[<span data-ttu-id="ea88e-221">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="ea88e-221">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

[<span data-ttu-id="ea88e-222">New-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="ea88e-222">New-AzADApplication</span></span>](./New-AzADApplication.md)

[<span data-ttu-id="ea88e-223">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="ea88e-223">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="ea88e-224">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="ea88e-224">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

[<span data-ttu-id="ea88e-225">New-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="ea88e-225">New-AzADSpCredential</span></span>](./New-AzADSpCredential.md)

[<span data-ttu-id="ea88e-226">Remove-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="ea88e-226">Remove-AzADSpCredential</span></span>](./Remove-AzADSpCredential.md)