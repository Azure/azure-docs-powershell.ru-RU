---
title: Создание субъекта-службы Azure с помощью Azure PowerShell
description: Создание субъекта-службы для приложения или службы с помощью Azure PowerShell.
keywords: Azure PowerShell, Azure Active Directory, Azure Active Directory, AD, RBAC
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/09/2018
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 76456b3d0e2a0c000488c0d7518845e5f56f2c75
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/01/2020
ms.locfileid: "89243333"
---
# <a name="create-an-azure-service-principal-with-azure-powershell"></a><span data-ttu-id="b4ad7-104">Создание субъекта-службы Azure с помощью Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="b4ad7-104">Create an Azure service principal with Azure PowerShell</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

<span data-ttu-id="b4ad7-105">Если вы планируете управлять приложением или службой с помощью Azure PowerShell, эти решения нужно запустить в субъекте-службе Azure Active Directory (AAD), а не своей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="b4ad7-105">If you plan to manage your app or service with Azure PowerShell, you should run it under an Azure Active Directory (AAD) service principal, rather than your own credentials.</span></span> <span data-ttu-id="b4ad7-106">В этой статье объясняется, как создать субъект безопасности с помощью Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b4ad7-106">This article steps you through creating a security principal with Azure PowerShell.</span></span>

> [!NOTE]
> <span data-ttu-id="b4ad7-107">Можно также создать субъект-службу на портале Azure.</span><span class="sxs-lookup"><span data-stu-id="b4ad7-107">You can also create a service principal through the Azure portal.</span></span> <span data-ttu-id="b4ad7-108">Дополнительные сведения см. в статье [Создание приложения Azure Active Directory и субъекта-службы с доступом к ресурсам с помощью портала](/azure/azure-resource-manager/resource-group-create-service-principal-portal).</span><span class="sxs-lookup"><span data-stu-id="b4ad7-108">Read [Use portal to create Active Directory application and service principal that can access resources](/azure/azure-resource-manager/resource-group-create-service-principal-portal) for more details.</span></span>

## <a name="what-is-a-service-principal"></a><span data-ttu-id="b4ad7-109">Что такое субъект-служба?</span><span class="sxs-lookup"><span data-stu-id="b4ad7-109">What is a 'service principal'?</span></span>

<span data-ttu-id="b4ad7-110">Субъект-служба Azure — это идентификатор безопасности, который созданные пользователем приложения, службы и средства автоматизации используют для доступа к определенным ресурсам Azure.</span><span class="sxs-lookup"><span data-stu-id="b4ad7-110">An Azure service principal is a security identity used by user-created apps, services, and automation tools to access specific Azure resources.</span></span> <span data-ttu-id="b4ad7-111">Это что-то вроде удостоверения пользователя (имя пользователя и пароль или сертификат) с определенной ролью и строго контролируемыми разрешениями.</span><span class="sxs-lookup"><span data-stu-id="b4ad7-111">Think of it as a 'user identity' (username and password or certificate) with a specific role, and tightly controlled permissions.</span></span> <span data-ttu-id="b4ad7-112">В отличие от удостоверений пользователей субъект-служба должен выполнять только определенные задачи.</span><span class="sxs-lookup"><span data-stu-id="b4ad7-112">A service principal should only need to do specific things, unlike a general user identity.</span></span> <span data-ttu-id="b4ad7-113">Это решение повышает безопасность, если вы предоставите ему минимальный уровень разрешений для выполнения задач управления.</span><span class="sxs-lookup"><span data-stu-id="b4ad7-113">It improves security if you only grant it the minimum permissions level needed to perform its management tasks.</span></span>

## <a name="verify-your-own-permission-level"></a><span data-ttu-id="b4ad7-114">Проверка уровня разрешений</span><span class="sxs-lookup"><span data-stu-id="b4ad7-114">Verify your own permission level</span></span>

<span data-ttu-id="b4ad7-115">Во-первых, у вас должен быть достаточный уровень разрешений в Azure Active Directory и подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="b4ad7-115">First, you must have sufficient permissions in both your Azure Active Directory and your Azure subscription.</span></span> <span data-ttu-id="b4ad7-116">У вас должно быть право создавать приложения в Active Directory и назначать роли субъекту-службе.</span><span class="sxs-lookup"><span data-stu-id="b4ad7-116">You must be able to create an app in the Active Directory and assign a role to the service principal.</span></span>

<span data-ttu-id="b4ad7-117">Проверить, есть ли у вас необходимые разрешения, проще всего на портале.</span><span class="sxs-lookup"><span data-stu-id="b4ad7-117">The easiest way to check whether your account has the right permissions is through the portal.</span></span> <span data-ttu-id="b4ad7-118">Ознакомьтесь с [проверкой наличия необходимых разрешений на портале](/azure/azure-resource-manager/resource-group-create-service-principal-portal#required-permissions).</span><span class="sxs-lookup"><span data-stu-id="b4ad7-118">See [Check required permission in portal](/azure/azure-resource-manager/resource-group-create-service-principal-portal#required-permissions).</span></span>

## <a name="create-a-service-principal-for-your-app"></a><span data-ttu-id="b4ad7-119">Создание субъекта-службы для приложения</span><span class="sxs-lookup"><span data-stu-id="b4ad7-119">Create a service principal for your app</span></span>

<span data-ttu-id="b4ad7-120">Войдите в учетную запись Azure, чтобы вы могли создать субъект-службу.</span><span class="sxs-lookup"><span data-stu-id="b4ad7-120">Once signed in to your Azure account, you can create the service principal.</span></span> <span data-ttu-id="b4ad7-121">Вам должен быть доступен один из следующих способов идентификации развернутого приложения:</span><span class="sxs-lookup"><span data-stu-id="b4ad7-121">You must have one of the following ways to identify your deployed app:</span></span>

* <span data-ttu-id="b4ad7-122">Уникальное имя развернутого приложения, например MyDemoWebApp в следующих примерах.</span><span class="sxs-lookup"><span data-stu-id="b4ad7-122">The unique name of your deployed app, such as "MyDemoWebApp" in the following examples, or</span></span>
* <span data-ttu-id="b4ad7-123">Идентификатор приложения, глобальный уникальный идентификатор, связанный с развернутым приложением, службой или объектом.</span><span class="sxs-lookup"><span data-stu-id="b4ad7-123">the Application ID, the unique GUID associated with your deployed app, service, or object</span></span>

### <a name="get-information-about-your-application"></a><span data-ttu-id="b4ad7-124">Получение сведений о приложении</span><span class="sxs-lookup"><span data-stu-id="b4ad7-124">Get information about your application</span></span>

<span data-ttu-id="b4ad7-125">Используйте командлет `Get-AzureRmADApplication`, чтобы получить сведения о приложении.</span><span class="sxs-lookup"><span data-stu-id="b4ad7-125">The `Get-AzureRmADApplication` cmdlet can be used to get information about your application.</span></span>

```azurepowershell-interactive
Get-AzureRmADApplication -DisplayNameStartWith MyDemoWebApp
```

```output
DisplayName             : MyDemoWebApp
ObjectId                : 775f64cd-0ec8-4b9b-b69a-8b8946022d9f
IdentifierUris          : {http://MyDemoWebApp}
HomePage                : http://www.contoso.com
Type                    : Application
ApplicationId           : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
AvailableToOtherTenants : False
AppPermissions          :
ReplyUrls               : {}
```

### <a name="create-a-service-principal-for-your-application"></a><span data-ttu-id="b4ad7-126">Создание субъекта-службы для приложения</span><span class="sxs-lookup"><span data-stu-id="b4ad7-126">Create a service principal for your application</span></span>

<span data-ttu-id="b4ad7-127">Используйте командлет `New-AzureRmADServicePrincipal`, чтобы создать субъект-службу.</span><span class="sxs-lookup"><span data-stu-id="b4ad7-127">The `New-AzureRmADServicePrincipal` cmdlet is used to create the service principal.</span></span>

```azurepowershell-interactive
$servicePrincipal = New-AzureRmADServicePrincipal -ApplicationId 00c01aaa-1603-49fc-b6df-b78c4e5138b4
```

```output
Secret                : System.Security.SecureString
ServicePrincipalNames : {00c01aaa-1603-49fc-b6df-b78c4e5138b4, http://MyDemoWebApp}
ApplicationId         : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
DisplayName           : MyDemoWebApp
Id                    : 698138e7-d7b6-4738-a866-b4e3081a69e4
AdfsId                :
Type                  : ServicePrincipal
```

<span data-ttu-id="b4ad7-128">Здесь вы можете либо непосредственно использовать свойство $servicePrincipal.Secret в командлете Connect-AzureRmAccount (см. раздел "Вход с помощью субъекта-службы" ниже), либо преобразовать SecureString в простую текстовую строку для дальнейшего использования:</span><span class="sxs-lookup"><span data-stu-id="b4ad7-128">From here, you can either directly use the $servicePrincipal.Secret property in Connect-AzureRmAccount (see "Sign in using the service principal" below), or you can convert this SecureString to a plain text string for later usage:</span></span>

```azurepowershell-interactive
$BSTR = [System.Runtime.InteropServices.Marshal]::SecureStringToBSTR($servicePrincipal.Secret)
$password = [System.Runtime.InteropServices.Marshal]::PtrToStringAuto($BSTR)
[Runtime.InteropServices.Marshal]::ZeroFreeBSTR($BSTR)
```

### <a name="sign-in-using-the-service-principal"></a><span data-ttu-id="b4ad7-129">Вход с помощью субъекта-службы</span><span class="sxs-lookup"><span data-stu-id="b4ad7-129">Sign in using the service principal</span></span>

<span data-ttu-id="b4ad7-130">Теперь вы можете выполнить вход от имени нового субъекта-службы для вашего приложения, используя указанный *appId* и автоматически созданный *пароль*.</span><span class="sxs-lookup"><span data-stu-id="b4ad7-130">You can now sign in as the new service principal for your app using the *appId* you provided and *password* that was automatically generated.</span></span> <span data-ttu-id="b4ad7-131">Для субъекта-службы также нужно указать идентификатор клиента.</span><span class="sxs-lookup"><span data-stu-id="b4ad7-131">You also need the Tenant ID for the service principal.</span></span> <span data-ttu-id="b4ad7-132">Идентификатор клиента отображается, если вы вошли в Azure с помощью личных учетных данных.</span><span class="sxs-lookup"><span data-stu-id="b4ad7-132">Your Tenant ID is displayed when you sign into Azure with your personal credentials.</span></span> <span data-ttu-id="b4ad7-133">Чтобы выполнить вход с помощью субъекта-службы, используйте следующие команды:</span><span class="sxs-lookup"><span data-stu-id="b4ad7-133">To sign in with a service principal, use the following commands:</span></span>

```azurepowershell-interactive
$cred = New-Object System.Management.Automation.PSCredential ("00c01aaa-1603-49fc-b6df-b78c4e5138b4", $servicePrincipal.Secret)
Connect-AzureRmAccount -Credential $cred -ServicePrincipal -TenantId XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
```

<span data-ttu-id="b4ad7-134">После успешного входа вы увидите примерно такие выходные данные:</span><span class="sxs-lookup"><span data-stu-id="b4ad7-134">After a successful sign-in you see output like:</span></span>

```output
Environment           : AzureCloud
Account               : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
SubscriptionId        :
SubscriptionName      :
CurrentStorageAccount :
```

<span data-ttu-id="b4ad7-135">Поздравляем!</span><span class="sxs-lookup"><span data-stu-id="b4ad7-135">Congratulations!</span></span> <span data-ttu-id="b4ad7-136">Эти учетные данные можно использовать для запуска приложения.</span><span class="sxs-lookup"><span data-stu-id="b4ad7-136">You can use these credentials to run your app.</span></span> <span data-ttu-id="b4ad7-137">Теперь необходимо настроить права субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="b4ad7-137">Next, you need to adjust the permissions of the service principal.</span></span>

## <a name="managing-roles"></a><span data-ttu-id="b4ad7-138">Управление ролями</span><span class="sxs-lookup"><span data-stu-id="b4ad7-138">Managing roles</span></span>

> [!NOTE]
> <span data-ttu-id="b4ad7-139">Управление доступом на основе ролей в Azure (RBAC) — это модель для определения ролей пользователя и субъектов-служб и управления этими ролями.</span><span class="sxs-lookup"><span data-stu-id="b4ad7-139">Azure Role-Based Access Control (RBAC) is a model for defining and managing roles for user and service principals.</span></span> <span data-ttu-id="b4ad7-140">Ролям назначаются связанные наборы разрешений, которые определяют ресурсы, доступные субъекту для чтения, доступа, записи или управления.</span><span class="sxs-lookup"><span data-stu-id="b4ad7-140">Roles have sets of permissions associated with them, which determine the resources a principal can read, access, write, or manage.</span></span> <span data-ttu-id="b4ad7-141">Дополнительные сведения об RBAC и ролях см. в статье [Встроенные роли для управления доступом на основе ролей в Azure](/azure/active-directory/role-based-access-built-in-roles).</span><span class="sxs-lookup"><span data-stu-id="b4ad7-141">For more information on RBAC and roles, see [RBAC: Built-in roles](/azure/active-directory/role-based-access-built-in-roles).</span></span>

<span data-ttu-id="b4ad7-142">В Azure PowerShell доступны следующие командлеты для управления назначением ролей:</span><span class="sxs-lookup"><span data-stu-id="b4ad7-142">Azure PowerShell provides the following cmdlets to manage role assignments:</span></span>

* [<span data-ttu-id="b4ad7-143">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="b4ad7-143">Get-AzureRmRoleAssignment</span></span>](/powershell/module/azurerm.resources/get-azurermroleassignment)
* [<span data-ttu-id="b4ad7-144">New-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="b4ad7-144">New-AzureRmRoleAssignment</span></span>](/powershell/module/azurerm.resources/new-azurermroleassignment)
* [<span data-ttu-id="b4ad7-145">Remove-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="b4ad7-145">Remove-AzureRmRoleAssignment</span></span>](/powershell/module/azurerm.resources/remove-azurermroleassignment)

<span data-ttu-id="b4ad7-146">По умолчанию субъекту-службе назначена роль **участника**.</span><span class="sxs-lookup"><span data-stu-id="b4ad7-146">The default role for a service principal is **Contributor**.</span></span> <span data-ttu-id="b4ad7-147">Возможно, это не лучший выбор для обеспечения взаимодействия приложения со службами Azure, учитывая общие разрешения этой роли.</span><span class="sxs-lookup"><span data-stu-id="b4ad7-147">It may not be the best choice depending on the scope of your app's interactions with Azure services, given its broad permissions.</span></span>
<span data-ttu-id="b4ad7-148">Роль **читателя** имеет больше ограничений и отлично подходит для приложений с доступом только на чтение.</span><span class="sxs-lookup"><span data-stu-id="b4ad7-148">The **Reader** role is more restrictive and can be a good choice for read-only apps.</span></span> <span data-ttu-id="b4ad7-149">Вы можете просмотреть сведения о разрешениях каждой роли или создать пользовательские разрешения на портале Azure.</span><span class="sxs-lookup"><span data-stu-id="b4ad7-149">You can view details on role-specific permissions or create custom ones through the Azure portal.</span></span>

<span data-ttu-id="b4ad7-150">В этом примере мы назначаем роль **читателя** предыдущему примеру субъекта-службы и удаляем роль **участника**:</span><span class="sxs-lookup"><span data-stu-id="b4ad7-150">In this example, we add the **Reader** role to our prior example, and delete the **Contributor** one:</span></span>

```azurepowershell-interactive
New-AzureRmRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4 -RoleDefinitionName Reader
```

```output
RoleAssignmentId   : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG/providers/Microsoft.Authorization/roleAssignments/818892f2-d075-46a1-a3a2-3a4e1a12fcd5
Scope              : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG
DisplayName        : MyDemoWebApp
SignInName         :
RoleDefinitionName : Reader
RoleDefinitionId   : b24988ac-6180-42a0-ab88-20f7382dd24c
ObjectId           : 698138e7-d7b6-4738-a866-b4e3081a69e4
ObjectType         : ServicePrincipal
```

```azurepowershell-interactive
Remove-AzureRmRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4 -RoleDefinitionName Contributor
```

<span data-ttu-id="b4ad7-151">Вот как просмотреть текущие назначенные роли:</span><span class="sxs-lookup"><span data-stu-id="b4ad7-151">To view the current roles assigned:</span></span>

```azurepowershell-interactive
Get-AzureRmRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4
```

```output
RoleAssignmentId   : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG/providers/Microsoft.Authorization/roleAssignments/0906bbd8-9982-4c03-8dae-aeaae8b13f9e
Scope              : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG
DisplayName        : MyDemoWebApp
SignInName         :
RoleDefinitionName : Reader
RoleDefinitionId   : acdd72a7-3385-48ef-bd42-f606fba81ae7
ObjectId           : 698138e7-d7b6-4738-a866-b4e3081a69e4
ObjectType         : ServicePrincipal
```

<span data-ttu-id="b4ad7-152">Другие командлеты Azure PowerShell для управления ролями:</span><span class="sxs-lookup"><span data-stu-id="b4ad7-152">Other Azure PowerShell cmdlets for role management:</span></span>

* [<span data-ttu-id="b4ad7-153">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="b4ad7-153">Get-AzureRmRoleDefinition</span></span>](/powershell/module/azurerm.resources/Get-AzureRmRoleDefinition)
* [<span data-ttu-id="b4ad7-154">New-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="b4ad7-154">New-AzureRmRoleDefinition</span></span>](/powershell/module/azurerm.resources/New-AzureRmRoleDefinition)
* [<span data-ttu-id="b4ad7-155">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="b4ad7-155">Remove-AzureRmRoleDefinition</span></span>](/powershell/module/azurerm.resources/Remove-AzureRmRoleDefinition)
* [<span data-ttu-id="b4ad7-156">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="b4ad7-156">Set-AzureRmRoleDefinition</span></span>](/powershell/module/azurerm.resources/Set-AzureRmRoleDefinition)

## <a name="change-the-credentials-of-the-security-principal"></a><span data-ttu-id="b4ad7-157">Изменение учетных данных субъекта безопасности</span><span class="sxs-lookup"><span data-stu-id="b4ad7-157">Change the credentials of the security principal</span></span>

<span data-ttu-id="b4ad7-158">Из соображений безопасности рекомендуется регулярно просматривать разрешения и обновлять пароли.</span><span class="sxs-lookup"><span data-stu-id="b4ad7-158">It's a good security practice to review the permissions and update the password regularly.</span></span> <span data-ttu-id="b4ad7-159">Можно также изменять учетные данные безопасности и управлять ими в случае изменения приложений.</span><span class="sxs-lookup"><span data-stu-id="b4ad7-159">You may also want to manage and modify the security credentials as your app changes.</span></span> <span data-ttu-id="b4ad7-160">Например, можно изменить пароль субъекта-службы, создав новый пароль и удалив старый.</span><span class="sxs-lookup"><span data-stu-id="b4ad7-160">For example, we can change the password of the service principal by creating a new password and removing the old one.</span></span>

### <a name="add-a-new-password-for-the-service-principal"></a><span data-ttu-id="b4ad7-161">Добавление нового пароля субъекта-службы</span><span class="sxs-lookup"><span data-stu-id="b4ad7-161">Add a new password for the service principal</span></span>

```azurepowershell-interactive
New-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```output
Secret    : System.Security.SecureString
StartDate : 11/16/2018 12:38:23 AM
EndDate   : 11/16/2019 12:38:23 AM
KeyId     : 6f801c3e-6fcd-42b9-be8e-320b17ba1d36
Type      : Password
```

### <a name="get-a-list-of-credentials-for-the-service-principal"></a><span data-ttu-id="b4ad7-162">Получение списка учетных данных субъекта-службы</span><span class="sxs-lookup"><span data-stu-id="b4ad7-162">Get a list of credentials for the service principal</span></span>

```azurepowershell-interactive
Get-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```output
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
5/5/2016 4:55:27 PM 5/5/2017 4:55:27 PM ca9d4846-4972-4c70-b6f5-a4effa60b9bc Password
```

### <a name="remove-the-old-password-from-the-service-principal"></a><span data-ttu-id="b4ad7-163">Удаление старого пароля субъекта-службы</span><span class="sxs-lookup"><span data-stu-id="b4ad7-163">Remove the old password from the service principal</span></span>

```azurepowershell-interactive
Remove-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp -KeyId ca9d4846-4972-4c70-b6f5-a4effa60b9bc
```

```output
Confirm
Are you sure you want to remove credential with keyId '6f801c3e-6fcd-42b9-be8e-320b17ba1d36' for
service principal objectId '698138e7-d7b6-4738-a866-b4e3081a69e4'.
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

### <a name="verify-the-list-of-credentials-for-the-service-principal"></a><span data-ttu-id="b4ad7-164">Проверка списка учетных данных субъекта-службы</span><span class="sxs-lookup"><span data-stu-id="b4ad7-164">Verify the list of credentials for the service principal</span></span>

```azurepowershell-interactive
Get-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```output
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
```

### <a name="get-information-about-the-service-principal"></a><span data-ttu-id="b4ad7-165">Получение сведений о субъекте-службе</span><span class="sxs-lookup"><span data-stu-id="b4ad7-165">Get information about the service principal</span></span>

```azurepowershell-interactive
$svcprincipal = Get-AzureRmADServicePrincipal -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4
$svcprincipal | Select-Object *
```

```output
ServicePrincipalNames : {http://MyDemoWebApp, 00c01aaa-1603-49fc-b6df-b78c4e5138b4}
ApplicationId         : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
DisplayName           : MyDemoWebApp
Id                    : 698138e7-d7b6-4738-a866-b4e3081a69e4
Type                  : ServicePrincipal
```
