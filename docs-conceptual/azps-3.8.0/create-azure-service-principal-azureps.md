---
title: Использование субъектов-служб Azure с помощью Azure PowerShell
description: В этой статье описывается, как создавать и использовать субъекты-службы с помощью Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/17/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: eae16ac1cdcb9ba456f9ad220854976544193299
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/01/2020
ms.locfileid: "89241412"
---
# <a name="create-an-azure-service-principal-with-azure-powershell"></a><span data-ttu-id="f6b37-103">Создание субъекта-службы Azure с помощью Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="f6b37-103">Create an Azure service principal with Azure PowerShell</span></span>

<span data-ttu-id="f6b37-104">Разрешения для автоматизированных средств, которые используют службы Azure, всегда должны быть ограничены.</span><span class="sxs-lookup"><span data-stu-id="f6b37-104">Automated tools that use Azure services should always have restricted permissions.</span></span> <span data-ttu-id="f6b37-105">В качестве замены входу в приложения с использованием учетной записи пользователя с полными правами Azure предлагает субъекты-службы.</span><span class="sxs-lookup"><span data-stu-id="f6b37-105">Instead of having applications sign in as a fully privileged user, Azure offers service principals.</span></span>

<span data-ttu-id="f6b37-106">Субъект-служба Azure — это удостоверение, созданное для использования с приложениями, размещенными службами и автоматизированными средствами с целью получения доступа к ресурсам Azure.</span><span class="sxs-lookup"><span data-stu-id="f6b37-106">An Azure service principal is an identity created for use with applications, hosted services, and automated tools to access Azure resources.</span></span> <span data-ttu-id="f6b37-107">Такой доступ ограничен ролями, которые назначены субъекту-службе, что позволяет управлять разрешениями доступа к ресурсам, в том числе на разных уровнях.</span><span class="sxs-lookup"><span data-stu-id="f6b37-107">This access is restricted by the roles assigned to the service principal, giving you control over which resources can be accessed and at which level.</span></span> <span data-ttu-id="f6b37-108">По соображениям безопасности мы рекомендуем всегда использовать субъекты-службы с автоматизированными средствами, чтобы не допускать их входа с помощью удостоверения пользователя.</span><span class="sxs-lookup"><span data-stu-id="f6b37-108">For security reasons, it's always recommended to use service principals with automated tools rather than allowing them to log in with a user identity.</span></span>

<span data-ttu-id="f6b37-109">В этой статье описано, как создать субъект-службу, получить сведения о нем и сбросить его с помощью Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f6b37-109">This article shows you the steps for creating, getting information about, and resetting a service principal with Azure PowerShell.</span></span>

## <a name="create-a-service-principal"></a><span data-ttu-id="f6b37-110">Создание субъекта-службы</span><span class="sxs-lookup"><span data-stu-id="f6b37-110">Create a service principal</span></span>

<span data-ttu-id="f6b37-111">Вы можете создать субъект-службу с помощью командлета [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal).</span><span class="sxs-lookup"><span data-stu-id="f6b37-111">Create a service principal with the [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal) cmdlet.</span></span> <span data-ttu-id="f6b37-112">При создании субъекта-службы вы задаете используемый им тип аутентификации для входа.</span><span class="sxs-lookup"><span data-stu-id="f6b37-112">When creating a service principal, you choose the type of sign-in authentication it uses.</span></span>

> [!NOTE]
> <span data-ttu-id="f6b37-113">Если у вашей учетной записи нет разрешения на создание субъекта-службы, командлет `New-AzADServicePrincipal` вернет сообщение об ошибке, информирующее о том, что у вас недостаточно привилегий для выполнения этой операции.</span><span class="sxs-lookup"><span data-stu-id="f6b37-113">If your account doesn't have permission to create a service principal, `New-AzADServicePrincipal` will return an error message containing "Insufficient privileges to complete the operation".</span></span>
> <span data-ttu-id="f6b37-114">Чтобы получить возможность создавать субъекты-службы, обратитесь к администратору Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f6b37-114">Contact your Azure Active Directory admin to create a service principal.</span></span>

<span data-ttu-id="f6b37-115">Субъектам-службам доступно два вида аутентификации: на основе пароля и на основе сертификата.</span><span class="sxs-lookup"><span data-stu-id="f6b37-115">There are two types of authentication available for service principals: Password-based authentication, and certificate-based authentication.</span></span>

### <a name="password-based-authentication"></a><span data-ttu-id="f6b37-116">Аутентификация на основе пароля</span><span class="sxs-lookup"><span data-stu-id="f6b37-116">Password-based authentication</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f6b37-117">Роль по умолчанию для субъекта-службы аутентификации на основе пароля — **Участник**.</span><span class="sxs-lookup"><span data-stu-id="f6b37-117">The default role for a password-based authentication service principal is **Contributor**.</span></span> <span data-ttu-id="f6b37-118">Эта роль имеет все разрешения на чтение из учетной записи Azure и запись в нее.</span><span class="sxs-lookup"><span data-stu-id="f6b37-118">This role has full permissions to read and write to an Azure account.</span></span> <span data-ttu-id="f6b37-119">Сведения о назначении ролей см. в разделе [Управление ролями субъекта-службы](#manage-service-principal-roles).</span><span class="sxs-lookup"><span data-stu-id="f6b37-119">For information on managing role assignments, see [Manage service principal roles](#manage-service-principal-roles).</span></span>

<span data-ttu-id="f6b37-120">Если другие параметры аутентификации не указаны, используется аутентификация на основе пароля, который генерируется случайным образом.</span><span class="sxs-lookup"><span data-stu-id="f6b37-120">Without any other authentication parameters, password-based authentication is used and a random password created for you.</span></span> <span data-ttu-id="f6b37-121">Это рекомендованный метод, если вам нужна аутентификация на основе пароля.</span><span class="sxs-lookup"><span data-stu-id="f6b37-121">If you want password-based authentication, this method is recommended.</span></span>

```azurepowershell-interactive
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName
```

<span data-ttu-id="f6b37-122">Возвращаемый объект содержит элемент `Secret`, который является строкой `SecureString` со сгенерированным паролем.</span><span class="sxs-lookup"><span data-stu-id="f6b37-122">The returned object contains the `Secret` member, which is a `SecureString` containing the generated password.</span></span> <span data-ttu-id="f6b37-123">Обязательно сохраните это значение в надежном расположении, чтобы выполнять аутентификацию с помощью субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="f6b37-123">Make sure that you store this value somewhere secure to authenticate with the service principal.</span></span> <span data-ttu-id="f6b37-124">Его значение _не будет_ отображаться в выходных данных консоли.</span><span class="sxs-lookup"><span data-stu-id="f6b37-124">Its value _won't_ be displayed in the console output.</span></span> <span data-ttu-id="f6b37-125">Если вы потеряли пароль, [сбросьте учетные данные субъекта-службы](#reset-credentials).</span><span class="sxs-lookup"><span data-stu-id="f6b37-125">If you lose the password, [reset the service principal credentials](#reset-credentials).</span></span>

<span data-ttu-id="f6b37-126">Следующий код позволяет экспортировать секрет:</span><span class="sxs-lookup"><span data-stu-id="f6b37-126">The following code will allow you to export the secret:</span></span>

```azurepowershell-interactive
$BSTR = [System.Runtime.InteropServices.Marshal]::SecureStringToBSTR($sp.Secret)
$UnsecureSecret = [System.Runtime.InteropServices.Marshal]::PtrToStringAuto($BSTR)
```

<span data-ttu-id="f6b37-127">Если вы используете предоставленные пользователями пароли, аргумент `-PasswordCredential` принимает объекты `Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential`.</span><span class="sxs-lookup"><span data-stu-id="f6b37-127">For user-supplied passwords, the `-PasswordCredential` argument takes `Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential` objects.</span></span> <span data-ttu-id="f6b37-128">Такие объекты должны иметь допустимые значения `StartDate` и `EndDate`, а также принимать значение `Password` в формате открытого текста.</span><span class="sxs-lookup"><span data-stu-id="f6b37-128">These objects must have a valid `StartDate` and `EndDate`, and take a plaintext `Password`.</span></span> <span data-ttu-id="f6b37-129">При создании пароля обязательно учитывайте [правила и ограничения для паролей в Azure Active Directory](/azure/active-directory/active-directory-passwords-policy).</span><span class="sxs-lookup"><span data-stu-id="f6b37-129">When creating a password, make sure you follow the [Azure Active Directory password rules and restrictions](/azure/active-directory/active-directory-passwords-policy).</span></span>
<span data-ttu-id="f6b37-130">Не используйте ненадежные пароли или пароли, которые уже используются вами для доступа к другим ресурсам.</span><span class="sxs-lookup"><span data-stu-id="f6b37-130">Don't use a weak password or reuse a password.</span></span>

```azurepowershell-interactive
Import-Module -Name Az.Resources # Imports the PSADPasswordCredential object
$credentials = New-Object Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential -Property @{StartDate=Get-Date; EndDate=Get-Date -Year 2024; Password=<Choose a strong password>}
$sp = New-AzAdServicePrincipal -DisplayName ServicePrincipalName -PasswordCredential $credentials
```

<span data-ttu-id="f6b37-131">Объект, возвращенный командлетом `New-AzADServicePrincipal`, содержит элементы `Id` и `DisplayName`, каждый из которых можно использовать для входа с помощью субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="f6b37-131">The object returned from `New-AzADServicePrincipal` contains the `Id` and `DisplayName` members, either of which can be used for sign in with the service principal.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f6b37-132">Вход с использованием субъекта-службы требует указания идентификатора клиента, для которого был создан субъект-служба.</span><span class="sxs-lookup"><span data-stu-id="f6b37-132">Signing in with a service principal requires the tenant ID which the service principal was created under.</span></span> <span data-ttu-id="f6b37-133">Чтобы получить данные об активном клиенте при создании субъекта-службы, выполните следующую команду _сразу же после_ создания субъекта-службы:</span><span class="sxs-lookup"><span data-stu-id="f6b37-133">To get the active tenant when the service principal was created, run the following command _immediately after_ service principal creation:</span></span>

```azurepowershell-interactive
(Get-AzContext).Tenant.Id
```

### <a name="certificate-based-authentication"></a><span data-ttu-id="f6b37-134">Аутентификация на основе сертификата</span><span class="sxs-lookup"><span data-stu-id="f6b37-134">Certificate-based authentication</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f6b37-135">При создании субъекта-службы аутентификации на основе сертификата роль по умолчанию не назначается.</span><span class="sxs-lookup"><span data-stu-id="f6b37-135">There is no default role assigned when creating a certificate-based authentication service principal.</span></span> <span data-ttu-id="f6b37-136">Сведения о назначении ролей см. в разделе [Управление ролями субъекта-службы](#manage-service-principal-roles).</span><span class="sxs-lookup"><span data-stu-id="f6b37-136">For information on managing role assignments, see [Manage service principal roles](#manage-service-principal-roles).</span></span>

<span data-ttu-id="f6b37-137">Субъекты-службы с аутентификацией на основе сертификата создаются с указанием параметра `-CertValue`.</span><span class="sxs-lookup"><span data-stu-id="f6b37-137">Service principals using certificate-based authentication are created with the `-CertValue` parameter.</span></span> <span data-ttu-id="f6b37-138">Этот параметр принимает строку ASCII открытого сертификата в кодировке Base64</span><span class="sxs-lookup"><span data-stu-id="f6b37-138">This parameter takes a base64-encoded ASCII string of the public certificate.</span></span> <span data-ttu-id="f6b37-139">в виде файла PEM, а также файла CRT или CER с текстовой кодировкой.</span><span class="sxs-lookup"><span data-stu-id="f6b37-139">This is represented by a PEM file, or a text-encoded CRT or CER.</span></span> <span data-ttu-id="f6b37-140">Двоичная кодировка открытых сертификатов не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="f6b37-140">Binary encodings of the public certificate aren't supported.</span></span> <span data-ttu-id="f6b37-141">При выполнении этих инструкций предполагается, что у вас уже есть сертификат.</span><span class="sxs-lookup"><span data-stu-id="f6b37-141">These instructions assume that you already have a certificate available.</span></span>

```azurepowershell-interactive
$cert = <public certificate as base64-encoded string>
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -CertValue $cert
```

<span data-ttu-id="f6b37-142">Вы также можете использовать параметр `-KeyCredential`, который принимает объекты `PSADKeyCredential`.</span><span class="sxs-lookup"><span data-stu-id="f6b37-142">You can also use the `-KeyCredential` parameter, which takes `PSADKeyCredential` objects.</span></span> <span data-ttu-id="f6b37-143">Такие объекты должны иметь допустимые значения `StartDate`, `EndDate`, а их элемент `CertValue` должен иметь значение строки ASCII открытого сертификата в кодировке Base64.</span><span class="sxs-lookup"><span data-stu-id="f6b37-143">These objects must have a valid `StartDate`, `EndDate`, and have the `CertValue` member set to a base64-encoded ASCII string of the public certificate.</span></span>

```azurepowershell-interactive
$cert = <public certificate as base64-encoded string>
$credentials = New-Object Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential -Property @{StartDate=Get-Date; EndDate=Get-Date -Year 2024; KeyId=New-Guid; CertValue=$cert}
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -KeyCredential $credentials
```

<span data-ttu-id="f6b37-144">Объект, возвращенный командлетом `New-AzADServicePrincipal`, содержит элементы `Id` и `DisplayName`, каждый из которых можно использовать для входа с помощью субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="f6b37-144">The object returned from `New-AzADServicePrincipal` contains the `Id` and `DisplayName` members, either of which can be used for sign in with the service principal.</span></span> <span data-ttu-id="f6b37-145">Клиентам, которые выполняют вход с использованием субъекта-службы, также нужен доступ к закрытому ключу сертификата.</span><span class="sxs-lookup"><span data-stu-id="f6b37-145">Clients which sign in with the service principal also need access to the certificate's private key.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f6b37-146">Вход с использованием субъекта-службы требует указания идентификатора клиента, для которого был создан субъект-служба.</span><span class="sxs-lookup"><span data-stu-id="f6b37-146">Signing in with a service principal requires the tenant ID which the service principal was created under.</span></span> <span data-ttu-id="f6b37-147">Чтобы получить данные об активном клиенте при создании субъекта-службы, выполните следующую команду _сразу же после_ создания субъекта-службы:</span><span class="sxs-lookup"><span data-stu-id="f6b37-147">To get the active tenant when the service principal was created, run the following command _immediately after_ service principal creation:</span></span>

```azurepowershell-interactive
(Get-AzContext).Tenant.Id
```

## <a name="get-an-existing-service-principal"></a><span data-ttu-id="f6b37-148">Получение существующего субъекта-службы</span><span class="sxs-lookup"><span data-stu-id="f6b37-148">Get an existing service principal</span></span>

<span data-ttu-id="f6b37-149">Список субъектов-служб для активного арендатора можно получить с помощью командлета [Get-AzADServicePrincipal](/powershell/module/az.resources/get-azadserviceprincipal).</span><span class="sxs-lookup"><span data-stu-id="f6b37-149">A list of service principals for the active tenant can be retrieved with [Get-AzADServicePrincipal](/powershell/module/az.resources/get-azadserviceprincipal).</span></span> <span data-ttu-id="f6b37-150">По умолчанию эта команда возвращает _все_ субъекты-службы в арендаторе.</span><span class="sxs-lookup"><span data-stu-id="f6b37-150">By default this command returns _all_ service principals in a tenant.</span></span> <span data-ttu-id="f6b37-151">Получение результатов для больших организаций может занять много времени.</span><span class="sxs-lookup"><span data-stu-id="f6b37-151">For large organizations, it may take a long time to return results.</span></span> <span data-ttu-id="f6b37-152">Поэтому мы рекомендуем использовать один из необязательных аргументов фильтрации на стороне сервера:</span><span class="sxs-lookup"><span data-stu-id="f6b37-152">Instead, using one of the optional server-side filtering arguments is recommended:</span></span>

- <span data-ttu-id="f6b37-153">`-DisplayNameBeginsWith` — запрашивает субъекты-службы с _префиксом_, который совпадает с указанным значением.</span><span class="sxs-lookup"><span data-stu-id="f6b37-153">`-DisplayNameBeginsWith` requests service principals that have a _prefix_ that match the provided value.</span></span> <span data-ttu-id="f6b37-154">Отображаемое имя субъекта-службы представляет собой значение, заданное при создании с помощью параметра `-DisplayName`.</span><span class="sxs-lookup"><span data-stu-id="f6b37-154">The display name of a service principal is the value set with `-DisplayName` during creation.</span></span>
- <span data-ttu-id="f6b37-155">`-DisplayName`  — запрашивает _точное совпадение_ для имени субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="f6b37-155">`-DisplayName` requests an _exact match_ of a service principal name.</span></span>

## <a name="manage-service-principal-roles"></a><span data-ttu-id="f6b37-156">Управление ролями субъекта-службы</span><span class="sxs-lookup"><span data-stu-id="f6b37-156">Manage service principal roles</span></span>

<span data-ttu-id="f6b37-157">В Azure PowerShell доступны следующие командлеты для управления назначением ролей:</span><span class="sxs-lookup"><span data-stu-id="f6b37-157">Azure PowerShell has the following cmdlets to manage role assignments:</span></span>

- [<span data-ttu-id="f6b37-158">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="f6b37-158">Get-AzRoleAssignment</span></span>](/powershell/module/az.resources/get-azroleassignment)
- [<span data-ttu-id="f6b37-159">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="f6b37-159">New-AzRoleAssignment</span></span>](/powershell/module/az.resources/new-azroleassignment)
- [<span data-ttu-id="f6b37-160">Remove-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="f6b37-160">Remove-AzRoleAssignment</span></span>](/powershell/module/az.resources/remove-azroleassignment)

<span data-ttu-id="f6b37-161">Роль по умолчанию для субъекта-службы аутентификации на основе пароля — **Участник**.</span><span class="sxs-lookup"><span data-stu-id="f6b37-161">The default role for a password-based authentication service principal is **Contributor**.</span></span> <span data-ttu-id="f6b37-162">Эта роль имеет все разрешения на чтение из учетной записи Azure и запись в нее.</span><span class="sxs-lookup"><span data-stu-id="f6b37-162">This role has full permissions to read and write to an Azure account.</span></span> <span data-ttu-id="f6b37-163">Роль **читателя** имеет больше ограничений, предоставляя права доступа только на чтение.</span><span class="sxs-lookup"><span data-stu-id="f6b37-163">The **Reader** role is more restrictive, with read-only access.</span></span> <span data-ttu-id="f6b37-164">Дополнительные сведения об управлении доступом на основе ролей см. в статье [Встроенные роли для управления доступом на основе ролей в Azure](/azure/active-directory/role-based-access-built-in-roles).</span><span class="sxs-lookup"><span data-stu-id="f6b37-164">For more information on Role-Based Access Control (RBAC) and roles, see [RBAC: Built-in roles](/azure/active-directory/role-based-access-built-in-roles).</span></span>

<span data-ttu-id="f6b37-165">В этом примере мы добавим роль **читателя** и удалим роль **участника**.</span><span class="sxs-lookup"><span data-stu-id="f6b37-165">This example adds the **Reader** role and removes the **Contributor** one:</span></span>

```azurepowershell-interactive
New-AzRoleAssignment -ApplicationId <service principal application ID> -RoleDefinitionName 'Reader'
Remove-AzRoleAssignment -ObjectId <service principal object ID> -RoleDefinitionName 'Contributor'
```

> [!IMPORTANT]
> <span data-ttu-id="f6b37-166">Командлеты назначения ролей не принимают идентификатор объекта субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="f6b37-166">Role assignment cmdlets don't take the service principal object ID.</span></span> <span data-ttu-id="f6b37-167">Они принимают связанный идентификатор приложения, который генерируется во время создания.</span><span class="sxs-lookup"><span data-stu-id="f6b37-167">They take the associated application ID, which is generated at creation time.</span></span> <span data-ttu-id="f6b37-168">Чтобы получить идентификатор приложения для субъекта-службы, воспользуйтесь командлетом `Get-AzADServicePrincipal`.</span><span class="sxs-lookup"><span data-stu-id="f6b37-168">To get the application ID for a service principal, use `Get-AzADServicePrincipal`.</span></span>

> [!NOTE]
> <span data-ttu-id="f6b37-169">Если у вашей учетной записи нет разрешения на назначение роли, вы увидите сообщение об ошибке, информирующее о том, что ваша учетная запись не авторизована для выполнения действия Microsoft.Authorization/roleAssignments/write.</span><span class="sxs-lookup"><span data-stu-id="f6b37-169">If your account doesn't have permission to assign a role, you see an error message that your account "does not have authorization to perform action 'Microsoft.Authorization/roleAssignments/write'".</span></span> <span data-ttu-id="f6b37-170">Чтобы получить возможность управлять ролями, обратитесь к администратору Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f6b37-170">Contact your Azure Active Directory admin to manage roles.</span></span>

<span data-ttu-id="f6b37-171">Добавление роли _не_ ограничивает назначенные ранее разрешения.</span><span class="sxs-lookup"><span data-stu-id="f6b37-171">Adding a role _doesn't_ restrict previously assigned permissions.</span></span> <span data-ttu-id="f6b37-172">При ограничении разрешений субъекта-службы обязательно удалите роль **участника**.</span><span class="sxs-lookup"><span data-stu-id="f6b37-172">When restricting a service principal's permissions, the **Contributor** role should be removed.</span></span>

<span data-ttu-id="f6b37-173">Чтобы проверить изменения, выведите назначенные роли:</span><span class="sxs-lookup"><span data-stu-id="f6b37-173">The changes can be verified by listing the assigned roles:</span></span>

```azurepowershell-interactive
Get-AzRoleAssignment -ServicePrincipalName ServicePrincipalName
```

## <a name="sign-in-using-a-service-principal"></a><span data-ttu-id="f6b37-174">Вход с помощью субъекта-службы</span><span class="sxs-lookup"><span data-stu-id="f6b37-174">Sign in using a service principal</span></span>

<span data-ttu-id="f6b37-175">Войдите, чтобы протестировать разрешения и учетные данные нового субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="f6b37-175">Test the new service principal's credentials and permissions by signing in.</span></span> <span data-ttu-id="f6b37-176">Чтобы войти с использованием субъекта-службы, вам нужно указать связанное с ним значение `applicationId` и клиент, для которого он был создан.</span><span class="sxs-lookup"><span data-stu-id="f6b37-176">To sign in with a service principal, you need the `applicationId` value associated with it, and the tenant it was created under.</span></span>

<span data-ttu-id="f6b37-177">Чтобы войти с использованием субъекта-службы с помощью пароля:</span><span class="sxs-lookup"><span data-stu-id="f6b37-177">To sign in with a service principal using a password:</span></span>

```azurepowershell-interactive
# Use the application ID as the username, and the secret as password
$credentials = Get-Credential
Connect-AzAccount -ServicePrincipal -Credential $credentials -Tenant <tenant ID>
```

<span data-ttu-id="f6b37-178">Для аутентификации на основе сертификата обязательно, чтобы среда Azure PowerShell могла извлекать данные из локального хранилища сертификатов по отпечатку сертификата.</span><span class="sxs-lookup"><span data-stu-id="f6b37-178">Certificate-based authentication requires that Azure PowerShell can retrieve information from a local certificate store based on a certificate thumbprint.</span></span>

```azurepowershell-interactive
Connect-AzAccount -ServicePrincipal -Tenant <tenant ID> -CertificateThumbprint <thumbprint>
```

<span data-ttu-id="f6b37-179">Инструкции по импорту сертификата в хранилище учетных записей, к которому имеет доступ PowerShell, см. в статье [Sign in with Azure PowerShell](authenticate-azureps.md#sp-signin) (Вход с помощью Azure PowerShell).</span><span class="sxs-lookup"><span data-stu-id="f6b37-179">For instructions on importing a certificate into a credential store accessible by PowerShell, see [Sign in with Azure PowerShell](authenticate-azureps.md#sp-signin)</span></span>

## <a name="reset-credentials"></a><span data-ttu-id="f6b37-180">Сброс учетных данных</span><span class="sxs-lookup"><span data-stu-id="f6b37-180">Reset credentials</span></span>

<span data-ttu-id="f6b37-181">Если вы забыли учетные данные для субъекта-службы, воспользуйтесь командлетом [New-AzADSpCredential](/powershell/module/az.resources/new-azadspcredential), чтобы добавить новые учетные данные с произвольным паролем.</span><span class="sxs-lookup"><span data-stu-id="f6b37-181">If you forget the credentials for a service principal, use [New-AzADSpCredential](/powershell/module/az.resources/new-azadspcredential) to add a new credential with a random password.</span></span> <span data-ttu-id="f6b37-182">Этот командлет не поддерживает определяемые пользователем учетные данные при сбросе пароля.</span><span class="sxs-lookup"><span data-stu-id="f6b37-182">This cmdlet does not support user-defined credentials when resetting the password.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f6b37-183">Прежде чем назначить новые учетные данные, удалите существующие, чтобы предотвратить вход с их использованием.</span><span class="sxs-lookup"><span data-stu-id="f6b37-183">Before assigning any new credentials, you may want to remove existing credentials to prevent sign in with them.</span></span> <span data-ttu-id="f6b37-184">Для этого выполните командлет [Remove-AzADSpCredential](/powershell/module/az.resources/remove-azadspcredential):</span><span class="sxs-lookup"><span data-stu-id="f6b37-184">To do so, use the [Remove-AzADSpCredential](/powershell/module/az.resources/remove-azadspcredential) cmdlet:</span></span>

```azurepowershell-interactive
Remove-AzADSpCredential -DisplayName ServicePrincipalName
```

```azurepowershell-interactive
$newCredential = New-AzADSpCredential -ServicePrincipalName ServicePrincipalName
```

## <a name="troubleshooting"></a><span data-ttu-id="f6b37-185">Устранение неполадок</span><span class="sxs-lookup"><span data-stu-id="f6b37-185">Troubleshooting</span></span>

<span data-ttu-id="f6b37-186">Если возникнет ошибка, сделайте следующее. _New-AzADServicePrincipal: Another object with the same value for property identifierUris already exists_ (New-AzADServicePrincipal: другой объект с таким же значением свойства identifierUris уже существует). Убедитесь, что субъект-служба с таким же именем не существует.</span><span class="sxs-lookup"><span data-stu-id="f6b37-186">If you receive the error: _"New-AzADServicePrincipal: Another object with the same value for property identifierUris already exists."_, verify that a service principal with the same name doesn't already exist.</span></span>

```azurepowershell-interactive
Get-AzAdServicePrincipal -DisplayName ServicePrincipalName
```

<span data-ttu-id="f6b37-187">Если существующий субъект-служба больше не нужен, его можно удалить, используя следующий пример.</span><span class="sxs-lookup"><span data-stu-id="f6b37-187">If the existing service principal is no longer needed, you can remove it using the following example.</span></span>

```azurepowershell-interactive
Remove-AzAdServicePrincipal -DisplayName ServicePrincipalName
```

<span data-ttu-id="f6b37-188">Эта ошибка также может возникать, если вы ранее создали субъект-службу для приложения Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f6b37-188">This error can also occur when you've previously created a service principal for an Azure Active Directory application.</span></span> <span data-ttu-id="f6b37-189">При удалении субъекта-службы приложение остается доступным.</span><span class="sxs-lookup"><span data-stu-id="f6b37-189">If you remove the service principal, the application is still available.</span></span> <span data-ttu-id="f6b37-190">Это приложение не позволяет создать другой субъект-службу с тем же именем.</span><span class="sxs-lookup"><span data-stu-id="f6b37-190">This application prevents you from creating another service principal with the same name.</span></span>

<span data-ttu-id="f6b37-191">Чтобы убедиться, что приложение Azure Active Directory с тем же именем не существует, можно использовать следующий пример.</span><span class="sxs-lookup"><span data-stu-id="f6b37-191">You can use the following example to verify that an Azure Active Directory application with the same name doesn't exist:</span></span>

```azurepowershell-interactive
Get-AzADApplication -DisplayName ServicePrincipalName
```

<span data-ttu-id="f6b37-192">Если приложение с тем же именем уже существует, но больше не требуется, его можно удалить, используя следующий пример.</span><span class="sxs-lookup"><span data-stu-id="f6b37-192">If an application with the same name does exist and is no longer needed, it can be removed using the following example.</span></span>

```azurepowershell-interactive
Remove-AzADApplication -DisplayName ServicePrincipalName
```

<span data-ttu-id="f6b37-193">В противном случае выберите другое имя для нового субъекта-службы, который вы пытаетесь создать.</span><span class="sxs-lookup"><span data-stu-id="f6b37-193">Otherwise, choose an alternate name for the new service principal that you're attempting to create.</span></span>
