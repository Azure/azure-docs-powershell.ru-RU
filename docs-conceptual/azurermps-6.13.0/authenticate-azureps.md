---
title: Вход с помощью Azure PowerShell
description: Сведения о том, как с помощью Azure PowerShell выполнить вход в роли пользователя, субъекта-службы или с помощью управляемых удостоверений для ресурсов Azure.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/09/2018
ms.openlocfilehash: e7a2368f2bbec625a8637d23650760115f506f76
ms.sourcegitcommit: 7839b82f47ef8dd522eff900081c22de0d089cfc
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "83387230"
---
# <a name="sign-in-with-azure-powershell"></a><span data-ttu-id="ae9ca-103">Вход с помощью Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="ae9ca-103">Sign in with Azure PowerShell</span></span>

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

<span data-ttu-id="ae9ca-104">Azure PowerShell поддерживает несколько методов проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="ae9ca-104">Azure PowerShell supports several authentication methods.</span></span> <span data-ttu-id="ae9ca-105">Проще всего начать со входа в интерактивном режиме из командной строки.</span><span class="sxs-lookup"><span data-stu-id="ae9ca-105">The simplest way to get started is to sign in interactively at the command line.</span></span>

## <a name="sign-in-interactively"></a><span data-ttu-id="ae9ca-106">Интерактивный вход</span><span class="sxs-lookup"><span data-stu-id="ae9ca-106">Sign in interactively</span></span>

<span data-ttu-id="ae9ca-107">Чтобы выполнить вход в интерактивном режиме, используйте командлет [Connect-AzureRmAccount](/powershell/module/azurerm.profile/connect-azurermaccount).</span><span class="sxs-lookup"><span data-stu-id="ae9ca-107">To sign in interactively, use the [Connect-AzureRmAccount](/powershell/module/azurerm.profile/connect-azurermaccount) cmdlet.</span></span>

```azurepowershell-interactive
Connect-AzureRmAccount
```

<span data-ttu-id="ae9ca-108">При выполнении этого командлета появится диалоговое окно с предложением ввести адрес электронной почты и пароль, связанные с учетной записью Azure.</span><span class="sxs-lookup"><span data-stu-id="ae9ca-108">When run, this cmdlet will bring up a dialog box prompting you for your email address and password associated with your Azure account.</span></span> <span data-ttu-id="ae9ca-109">Эта операция проверки подлинности актуальна для текущего сеанса PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ae9ca-109">This authentication lasts for the current PowerShell session.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ae9ca-110">Начиная с Azure PowerShell 6.3.0, можно использовать одни учетные данные в нескольких сеансах PowerShell, пока вы остаетесь в системе Windows.</span><span class="sxs-lookup"><span data-stu-id="ae9ca-110">As of Azure PowerShell 6.3.0, your credentials are shared among multiple PowerShell sessions as long as you remain signed in to Windows.</span></span> <span data-ttu-id="ae9ca-111">Дополнительные сведения см. в статье [Использование учетных данных пользователя в разных сеансах PowerShell](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="ae9ca-111">For more information, see the article on [Persistent Credentials](context-persistence.md).</span></span>

## <a name="sign-in-with-a-service-principal"></a><span data-ttu-id="ae9ca-112">Вход с использованием субъекта-службы</span><span class="sxs-lookup"><span data-stu-id="ae9ca-112">Sign in with a service principal</span></span>

<span data-ttu-id="ae9ca-113">Субъекты-службы не являются интерактивными учетными записями Azure.</span><span class="sxs-lookup"><span data-stu-id="ae9ca-113">Service principals are non-interactive Azure accounts.</span></span> <span data-ttu-id="ae9ca-114">Как и для других учетных записей пользователей, для управления их разрешениями используется Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ae9ca-114">Like other user accounts, their permissions are managed with Azure Active Directory.</span></span> <span data-ttu-id="ae9ca-115">Предоставив субъекту-службе только необходимые разрешения, вы обеспечите защиту скриптов автоматизации.</span><span class="sxs-lookup"><span data-stu-id="ae9ca-115">By granting a service principal only the permissions it needs, your automation scripts stay secure.</span></span>

<span data-ttu-id="ae9ca-116">Сведения о том, как создать субъект-службу для использования с помощью Azure PowerShell, см. в [этой статье](create-azure-service-principal-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="ae9ca-116">To learn how to create a service principal for use with Azure PowerShell, see [Create an Azure service principal with Azure PowerShell](create-azure-service-principal-azureps.md).</span></span>

<span data-ttu-id="ae9ca-117">Чтобы выполнить вход с помощью субъекта-службы, используйте аргумент `-ServicePrincipal` с командлетом `Connect-AzureRmAccount`.</span><span class="sxs-lookup"><span data-stu-id="ae9ca-117">To sign in with a service principal, use the `-ServicePrincipal` argument with the `Connect-AzureRmAccount` cmdlet.</span></span> <span data-ttu-id="ae9ca-118">Вам также потребуются учетные данные субъекта-службы и идентификатор клиента, связанный с субъектом-службой.</span><span class="sxs-lookup"><span data-stu-id="ae9ca-118">You'll also need the service principal's sign-in credentials and the tenant ID associated with the service principal.</span></span> <span data-ttu-id="ae9ca-119">Чтобы получить учетные данные субъекта-службы как соответствующий объект, используйте командлет [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential).</span><span class="sxs-lookup"><span data-stu-id="ae9ca-119">To get the service principal's credentials as the appropriate object, use the [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet.</span></span> <span data-ttu-id="ae9ca-120">Этот командлет вызовет диалоговое окно, в котором нужно ввести идентификатор пользователя и пароль субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="ae9ca-120">This cmdlet will display a dialog box to enter the service principal user ID and password into.</span></span>

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzureRmAccount -ServicePrincipal -Credential $pscredential -TenantId $tenantid
```

## <a name="sign-in-using-an-azure-managed-service-identity"></a><span data-ttu-id="ae9ca-121">Вход с использованием Управляемого удостоверения службы Azure</span><span class="sxs-lookup"><span data-stu-id="ae9ca-121">Sign in using an Azure Managed Service Identity</span></span>

<span data-ttu-id="ae9ca-122">Управляемые удостоверения для ресурсов Azure — это функция Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ae9ca-122">Managed identities for Azure resources is a feature of Azure Active Directory.</span></span> <span data-ttu-id="ae9ca-123">Вы можете использовать субъект-службу управляемых удостоверений для входа и получения маркера доступа только для приложений, обеспечив возможность обращения к другим ресурсам.</span><span class="sxs-lookup"><span data-stu-id="ae9ca-123">You can use a managed identity service principal for sign-in, and acquire an app-only access token to access other resources.</span></span> <span data-ttu-id="ae9ca-124">Управляемые удостоверения доступны только на виртуальных машинах в облаке Azure.</span><span class="sxs-lookup"><span data-stu-id="ae9ca-124">Managed identities are only available on virtual machines running in an Azure cloud.</span></span>

<span data-ttu-id="ae9ca-125">Дополнительные сведения об управляемых удостоверениях для ресурсов Azure см. в руководстве по [использованию управляемых удостоверений для ресурсов Azure на виртуальной машине Azure для получения маркера доступа](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span><span class="sxs-lookup"><span data-stu-id="ae9ca-125">For more information about managed identities for Azure resources, see [How to use managed identities for Azure resources on an Azure VM to acquire an access token](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span></span>

## <a name="sign-in-as-a-cloud-solution-provider-csp"></a><span data-ttu-id="ae9ca-126">Вход в качестве поставщика облачных решений</span><span class="sxs-lookup"><span data-stu-id="ae9ca-126">Sign in as a Cloud Solution Provider (CSP)</span></span>

<span data-ttu-id="ae9ca-127">Чтобы войти как [поставщик облачных решений (CSP)](https://azure.microsoft.com/offers/ms-azr-0145p/), используйте параметр `-TenantId`.</span><span class="sxs-lookup"><span data-stu-id="ae9ca-127">A [Cloud Solution Provider (CSP)](https://azure.microsoft.com/offers/ms-azr-0145p/) sign-in requires the use of `-TenantId`.</span></span> <span data-ttu-id="ae9ca-128">Как правило, этот параметр может быть предоставлен как идентификатор клиента или доменное имя.</span><span class="sxs-lookup"><span data-stu-id="ae9ca-128">Normally, this parameter can be provided as either a tenant ID or a domain name.</span></span> <span data-ttu-id="ae9ca-129">Но для входа в качестве поставщика облачных решений нужно указать **идентификатор клиента**.</span><span class="sxs-lookup"><span data-stu-id="ae9ca-129">However, for CSP sign-in, it must be provided a **tenant ID**.</span></span>

```azurepowershell-interactive
Connect-AzureRmAccount -TenantId 'xxxx-xxxx-xxxx-xxxx'
```

## <a name="sign-in-to-another-cloud"></a><span data-ttu-id="ae9ca-130">Вход в другое облако</span><span class="sxs-lookup"><span data-stu-id="ae9ca-130">Sign in to another Cloud</span></span>

<span data-ttu-id="ae9ca-131">Облачные службы Azure предоставляют среды, которые соответствуют региональным правилам обработки данных.</span><span class="sxs-lookup"><span data-stu-id="ae9ca-131">Azure cloud services offer environments compliant with regional data-handling regulations.</span></span>
<span data-ttu-id="ae9ca-132">Для учетных записей в региональном облаке нужно при входе указать среду с помощью аргумента `-Environment`.</span><span class="sxs-lookup"><span data-stu-id="ae9ca-132">For accounts in a regional cloud, set the environment when you sign in with the `-Environment` argument.</span></span>
<span data-ttu-id="ae9ca-133">Например, если ваша учетная запись находится в облаке для Китая, укажите следующее:</span><span class="sxs-lookup"><span data-stu-id="ae9ca-133">For example, if your account is in the China cloud:</span></span>

```azurepowershell-interactive
Connect-AzureRmAccount -Environment AzureChinaCloud
```

<span data-ttu-id="ae9ca-134">Следующая команда позволяет получить список доступных сред:</span><span class="sxs-lookup"><span data-stu-id="ae9ca-134">The following command gets a list of available environments:</span></span>

```azurepowershell-interactive
Get-AzureRmEnvironment | Select-Object Name
```

## <a name="learn-more-about-managing-azure-role-based-access"></a><span data-ttu-id="ae9ca-135">Узнайте больше об управлении доступом на основе ролей Azure</span><span class="sxs-lookup"><span data-stu-id="ae9ca-135">Learn more about managing Azure role-based access</span></span>

<span data-ttu-id="ae9ca-136">Дополнительные сведения об аутентификации и управлении подписками в Azure см. в статье [Использование назначений ролей для управления доступом к ресурсам в подписке Azure](/azure/active-directory/role-based-access-control-configure).</span><span class="sxs-lookup"><span data-stu-id="ae9ca-136">For more information about authentication and subscription management in Azure, see [Manage Accounts, Subscriptions, and Administrative Roles](/azure/active-directory/role-based-access-control-configure).</span></span>

<span data-ttu-id="ae9ca-137">Командлеты Azure PowerShell для управления ролями:</span><span class="sxs-lookup"><span data-stu-id="ae9ca-137">Azure PowerShell cmdlets for role management:</span></span>

* [<span data-ttu-id="ae9ca-138">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="ae9ca-138">Get-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/Get-AzureRmRoleAssignment)
* [<span data-ttu-id="ae9ca-139">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="ae9ca-139">Get-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Get-AzureRmRoleDefinition)
* [<span data-ttu-id="ae9ca-140">New-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="ae9ca-140">New-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/New-AzureRmRoleAssignment)
* [<span data-ttu-id="ae9ca-141">New-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="ae9ca-141">New-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/New-AzureRmRoleDefinition)
* [<span data-ttu-id="ae9ca-142">Remove-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="ae9ca-142">Remove-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleAssignment)
* [<span data-ttu-id="ae9ca-143">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="ae9ca-143">Remove-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleDefinition)
* [<span data-ttu-id="ae9ca-144">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="ae9ca-144">Set-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Set-AzureRmRoleDefinition)
