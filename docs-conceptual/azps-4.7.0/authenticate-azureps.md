---
title: Вход с помощью Azure PowerShell
description: Сведения о том, как с помощью Azure PowerShell выполнить вход в роли пользователя, субъекта-службы или с помощью управляемых удостоверений для ресурсов Azure.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 7/7/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 8f18af8ed67ecf2aefd353208c07bf812df732d9
ms.sourcegitcommit: 15f21c40dcb7610e2fbaaabf264ad925e4224500
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/22/2020
ms.locfileid: "90928576"
---
# <a name="sign-in-with-azure-powershell"></a><span data-ttu-id="2b065-103">Вход с помощью Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="2b065-103">Sign in with Azure PowerShell</span></span>

<span data-ttu-id="2b065-104">Azure PowerShell поддерживает несколько методов проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="2b065-104">Azure PowerShell supports several authentication methods.</span></span> <span data-ttu-id="2b065-105">Проще всего приступить к работе можно с помощью оболочки [Azure Cloud Shell](/azure/cloud-shell/overview), которая автоматически выполняет вход в вашу учетную запись.</span><span class="sxs-lookup"><span data-stu-id="2b065-105">The easiest way to get started is with [Azure Cloud Shell](/azure/cloud-shell/overview), which automatically logs you in.</span></span> <span data-ttu-id="2b065-106">Если используется локальная установка, вы можете выполнить вход в интерактивном режиме с помощью браузера.</span><span class="sxs-lookup"><span data-stu-id="2b065-106">With a local install, you can sign in interactively through your browser.</span></span> <span data-ttu-id="2b065-107">При написании скриптов автоматизации рекомендуется использовать [субъект-службу](create-azure-service-principal-azureps.md) с необходимыми разрешениями.</span><span class="sxs-lookup"><span data-stu-id="2b065-107">When writing scripts for automation, the recommended approach is to use a [service principal](create-azure-service-principal-azureps.md) with the necessary permissions.</span></span> <span data-ttu-id="2b065-108">Максимально ограничьте разрешения на вход для своего варианта использования, чтобы обеспечить защиту ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="2b065-108">When you restrict sign-in permissions as much as possible for your use case, you help keep your Azure resources secure.</span></span>

<span data-ttu-id="2b065-109">Если у вас есть доступ более чем к одной подписке, вы входите в первую, которую предлагает Azure.</span><span class="sxs-lookup"><span data-stu-id="2b065-109">Initially, you're signed into the first subscription Azure returns if you have access to more than one subscription.</span></span> <span data-ttu-id="2b065-110">Команды выполняются для этой подписки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2b065-110">Commands are run against this subscription by default.</span></span> <span data-ttu-id="2b065-111">Чтобы изменить активную подписку для сеанса, используйте командлет [Set-AzContext](/powershell/module/az.accounts/set-azcontext).</span><span class="sxs-lookup"><span data-stu-id="2b065-111">To change your active subscription for a session, use the [Set-AzContext](/powershell/module/az.accounts/set-azcontext) cmdlet.</span></span> <span data-ttu-id="2b065-112">Чтобы изменить активную подписку и сохранить ее между сеансами в той же системе, используйте командлет [Select-AzContext](/powershell/module/az.accounts/select-azcontext).</span><span class="sxs-lookup"><span data-stu-id="2b065-112">To change your active subscription and have it persist between sessions on the same system, use the [Select-AzContext](/powershell/module/az.accounts/select-azcontext) cmdlet.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2b065-113">Одни учетные данные можно использовать в нескольких сеансах PowerShell, пока вы остаетесь в системе.</span><span class="sxs-lookup"><span data-stu-id="2b065-113">Your credentials are shared among multiple PowerShell sessions as long as you remain signed in.</span></span>
> <span data-ttu-id="2b065-114">Дополнительные сведения см. в статье [Использование учетных данных пользователя в разных сеансах PowerShell](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="2b065-114">For more information, see the article on [Persistent Credentials](context-persistence.md).</span></span>

## <a name="sign-in-interactively"></a><span data-ttu-id="2b065-115">Интерактивный вход</span><span class="sxs-lookup"><span data-stu-id="2b065-115">Sign in interactively</span></span>

<span data-ttu-id="2b065-116">Чтобы выполнить вход в интерактивном режиме, используйте командлет [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount).</span><span class="sxs-lookup"><span data-stu-id="2b065-116">To sign in interactively, use the [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount) cmdlet.</span></span>

```azurepowershell-interactive
Connect-AzAccount
```

<span data-ttu-id="2b065-117">При запуске из PowerShell версии 6 и выше этот командлет предоставляет строку токена.</span><span class="sxs-lookup"><span data-stu-id="2b065-117">When run from PowerShell version 6 and higher, this cmdlet presents a token string.</span></span> <span data-ttu-id="2b065-118">Чтобы войти в систему, скопируйте эту строку и вставьте ее в строку [microsoft.com/devicelogin](https://microsoft.com/devicelogin) в веб-браузере.</span><span class="sxs-lookup"><span data-stu-id="2b065-118">To sign in, copy this string and paste it into [microsoft.com/devicelogin](https://microsoft.com/devicelogin) in a web browser.</span></span> <span data-ttu-id="2b065-119">Сеанс PowerShell пройдет аутентификацию для подключения к Azure.</span><span class="sxs-lookup"><span data-stu-id="2b065-119">Your PowerShell session will be authenticated to connect to Azure.</span></span> <span data-ttu-id="2b065-120">Можно указать параметр `UseDeviceAuthentication`, чтобы получить строку токена в Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2b065-120">You can specify the `UseDeviceAuthentication` parameter to receive a token string on Windows PowerShell.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2b065-121">Авторизация с учетными данными (на основе имени пользователя и пароля) была отключена в Azure PowerShell из-за изменений в способах авторизации Active Directory и по соображениям безопасности.</span><span class="sxs-lookup"><span data-stu-id="2b065-121">Username/password credential authorization has been removed in Azure PowerShell due to changes in Active Directory authorization implementations and security concerns.</span></span> <span data-ttu-id="2b065-122">Если вы используете авторизацию с учетными данными, чтобы автоматизировать процесс, [создайте субъект-службу](create-azure-service-principal-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="2b065-122">If you use credential authorization for automation purposes, instead [create a service principal](create-azure-service-principal-azureps.md).</span></span>

<span data-ttu-id="2b065-123">Используйте командлет [Get-AzContext](/powershell/module/az.accounts/get-azcontext), чтобы сохранить идентификатор арендатора в переменной, которая будет использоваться в следующих двух разделах этой статьи.</span><span class="sxs-lookup"><span data-stu-id="2b065-123">Use the [Get-AzContext](/powershell/module/az.accounts/get-azcontext) cmdlet to store your tenant ID in a variable to be used in the next two sections of this article.</span></span>

```azurepowershell-interactive
$tenantId = (Get-AzContext).Tenant.Id
```

## <a name="sign-in-with-a-service-principal"></a><span data-ttu-id="2b065-124">Вход с использованием субъекта-службы <a name="sp-signin"/></span><span class="sxs-lookup"><span data-stu-id="2b065-124">Sign in with a service principal <a name="sp-signin"/></span></span>

<span data-ttu-id="2b065-125">Субъекты-службы не являются интерактивными учетными записями Azure.</span><span class="sxs-lookup"><span data-stu-id="2b065-125">Service principals are non-interactive Azure accounts.</span></span> <span data-ttu-id="2b065-126">Как и для других учетных записей пользователей, для управления их разрешениями используется Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="2b065-126">Like other user accounts, their permissions are managed with Azure Active Directory.</span></span> <span data-ttu-id="2b065-127">Предоставив субъекту-службе только необходимые разрешения, вы обеспечите защиту скриптов автоматизации.</span><span class="sxs-lookup"><span data-stu-id="2b065-127">By granting a service principal only the permissions it needs, your automation scripts stay secure.</span></span>

<span data-ttu-id="2b065-128">Сведения о том, как создать субъект-службу для использования с помощью Azure PowerShell, см. в [этой статье](create-azure-service-principal-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="2b065-128">To learn how to create a service principal for use with Azure PowerShell, see [Create an Azure service principal with Azure PowerShell](create-azure-service-principal-azureps.md).</span></span>

<span data-ttu-id="2b065-129">Чтобы выполнить вход с помощью субъекта-службы, используйте аргумент `-ServicePrincipal` с командлетом `Connect-AzAccount`.</span><span class="sxs-lookup"><span data-stu-id="2b065-129">To sign in with a service principal, use the `-ServicePrincipal` argument with the `Connect-AzAccount` cmdlet.</span></span> <span data-ttu-id="2b065-130">Также потребуется идентификатор приложения субъекта-службы, учетные данные для входа и сопоставление идентификатора клиента с субъектом-службой.</span><span class="sxs-lookup"><span data-stu-id="2b065-130">You'll also need the service principal's application ID, sign-in credentials, and the tenant ID associate with the service principal.</span></span> <span data-ttu-id="2b065-131">Способ входа с использованием субъекта-службы зависит от способа аутентификации: на основе пароля или сертификата.</span><span class="sxs-lookup"><span data-stu-id="2b065-131">How you sign in with a service principal depends on whether it's configured for password-based or certificate-based authentication.</span></span>

### <a name="password-based-authentication"></a><span data-ttu-id="2b065-132">Аутентификация на основе пароля</span><span class="sxs-lookup"><span data-stu-id="2b065-132">Password-based authentication</span></span>

<span data-ttu-id="2b065-133">Создайте субъект-службу для использования в примерах в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="2b065-133">Create a service principal to be used in the examples in this section.</span></span> <span data-ttu-id="2b065-134">См. статью [Создание субъекта-службы Azure с помощью Azure PowerShell](/powershell/azure/create-azure-service-principal-azureps).</span><span class="sxs-lookup"><span data-stu-id="2b065-134">For more information on creating service principals, see [Create an Azure service principal with Azure PowerShell](/powershell/azure/create-azure-service-principal-azureps).</span></span>

```azurepowershell-interactive
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName
```

<span data-ttu-id="2b065-135">Чтобы получить учетные данные субъекта-службы как соответствующий объект, используйте командлет [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential).</span><span class="sxs-lookup"><span data-stu-id="2b065-135">To get the service principal's credentials as the appropriate object, use the [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet.</span></span> <span data-ttu-id="2b065-136">Этот командлет отображает запрос на ввод имени пользователя и пароля.</span><span class="sxs-lookup"><span data-stu-id="2b065-136">This cmdlet presents a prompt for a username and password.</span></span> <span data-ttu-id="2b065-137">Используйте значение `applicationID` субъекта-службы в качестве имени пользователя и преобразуйте значение `secret` в обычный текст для пароля.</span><span class="sxs-lookup"><span data-stu-id="2b065-137">Use the service principal's `applicationID` for the username and convert its `secret` to plain text for the password.</span></span>

```azurepowershell-interactive
# Retrieve the plain text password for use with `Get-Credential` in the next command.
$sp.secret | ConvertFrom-SecureString -AsPlainText

$pscredential = Get-Credential -UserName $sp.ApplicationId
Connect-AzAccount -ServicePrincipal -Credential $pscredential -Tenant $tenantId
```

<span data-ttu-id="2b065-138">В сценариях автоматизации вам нужно создать учетные данные на основе значений `applicationId` и `secret`субъекта-службы:</span><span class="sxs-lookup"><span data-stu-id="2b065-138">For automation scenarios, you need to create credentials from a service principal's `applicationId` and `secret`:</span></span>

```azurepowershell-interactive
$pscredential = New-Object -TypeName System.Management.Automation.PSCredential($sp.ApplicationId, $sp.Secret)
Connect-AzAccount -ServicePrincipal -Credential $pscredential -Tenant $tenantId
```

<span data-ttu-id="2b065-139">При автоматизации подключений субъекта-службы обязательно придерживайтесь рекомендаций по использованию паролей.</span><span class="sxs-lookup"><span data-stu-id="2b065-139">Make sure that you use good password storage practices when automating service principal connections.</span></span>

### <a name="certificate-based-authentication"></a><span data-ttu-id="2b065-140">Аутентификация на основе сертификата</span><span class="sxs-lookup"><span data-stu-id="2b065-140">Certificate-based authentication</span></span>

<span data-ttu-id="2b065-141">Для аутентификации на основе сертификата обязательно, чтобы среда Azure PowerShell могла извлекать данные из локального хранилища сертификатов по отпечатку сертификата.</span><span class="sxs-lookup"><span data-stu-id="2b065-141">Certificate-based authentication requires that Azure PowerShell can retrieve information from a local certificate store based on a certificate thumbprint.</span></span>

```azurepowershell-interactive
Connect-AzAccount -ApplicationId $appId -Tenant $tenantId -CertificateThumbprint <thumbprint>
```

<span data-ttu-id="2b065-142">При использовании субъекта-службы вместо зарегистрированного приложения добавьте аргумент `-ServicePrincipal` и предоставьте идентификатор приложения субъекта-службы в качестве значения параметра `-ApplicationId`.</span><span class="sxs-lookup"><span data-stu-id="2b065-142">When using a service principal instead of a registered application, add the `-ServicePrincipal` argument and provide the service principal's Application ID as the `-ApplicationId` parameter's value.</span></span>

```azurepowershell-interactive
Connect-AzAccount -ServicePrincipal -ApplicationId $servicePrincipalId -Tenant $tenantId -CertificateThumbprint <thumbprint>
```

<span data-ttu-id="2b065-143">В PowerShell 5.1 проверять и администрировать хранилище сертификатов можно с помощью модуля [PKI](/powershell/module/pkiclient).</span><span class="sxs-lookup"><span data-stu-id="2b065-143">In PowerShell 5.1, the certificate store can be managed and inspected with the [PKI](/powershell/module/pkiclient) module.</span></span> <span data-ttu-id="2b065-144">В PowerShell версии 6.х и выше это не настолько просто.</span><span class="sxs-lookup"><span data-stu-id="2b065-144">For PowerShell Core 6.x and later, the process is more complicated.</span></span> <span data-ttu-id="2b065-145">Приведенные ниже скрипты демонстрируют, как импортировать существующий сертификат в хранилище сертификатов, к которому имеет доступ PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2b065-145">The following scripts show you how to import an existing certificate into the certificate store accessible by PowerShell.</span></span>

#### <a name="import-a-certificate-in-powershell-51"></a><span data-ttu-id="2b065-146">Импорт сертификата в PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="2b065-146">Import a certificate in PowerShell 5.1</span></span>

```azurepowershell-interactive
# Import a PFX
$credentials = Get-Credential -Message "Provide PFX private key password"
Import-PfxCertificate -FilePath <path to certificate> -Password $credentials.Password -CertStoreLocation cert:\CurrentUser\My
```

#### <a name="import-a-certificate-in-powershell-core-6x-and-later"></a><span data-ttu-id="2b065-147">Импорт сертификата в PowerShell версии 6.х и выше</span><span class="sxs-lookup"><span data-stu-id="2b065-147">Import a certificate in PowerShell Core 6.x and later</span></span>

```azurepowershell-interactive
# Import a PFX
$storeName = [System.Security.Cryptography.X509Certificates.StoreName]::My
$storeLocation = [System.Security.Cryptography.X509Certificates.StoreLocation]::CurrentUser
$store = [System.Security.Cryptography.X509Certificates.X509Store]::new($storeName, $storeLocation)
$certPath = <path to certificate>
$credentials = Get-Credential -Message "Provide PFX private key password"
$flag = [System.Security.Cryptography.X509Certificates.X509KeyStorageFlags]::Exportable
$certificate = [System.Security.Cryptography.X509Certificates.X509Certificate2]::new($certPath, $credentials.Password, $flag)
$store.Open([System.Security.Cryptography.X509Certificates.OpenFlags]::ReadWrite)
$store.Add($Certificate)
$store.Close()
```

## <a name="sign-in-using-a-managed-identity"></a><span data-ttu-id="2b065-148">Вход с использованием управляемого удостоверения</span><span class="sxs-lookup"><span data-stu-id="2b065-148">Sign in using a managed identity</span></span>

<span data-ttu-id="2b065-149">Управляемые удостоверения — это функция Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="2b065-149">Managed identities are a feature of Azure Active Directory.</span></span> <span data-ttu-id="2b065-150">Они представляют собой субъекты-службы, назначенные ресурсам в Azure.</span><span class="sxs-lookup"><span data-stu-id="2b065-150">Managed identities are service principals assigned to resources that run in Azure.</span></span> <span data-ttu-id="2b065-151">Вы можете использовать субъект-службу управляемых удостоверений для входа и получения маркера доступа только для приложений, обеспечив возможность обращения к другим ресурсам.</span><span class="sxs-lookup"><span data-stu-id="2b065-151">You can use a managed identity service principal for sign-in, and acquire an app-only access token to access other resources.</span></span> <span data-ttu-id="2b065-152">Управляемые удостоверения доступны только в ресурсах в облаке Azure.</span><span class="sxs-lookup"><span data-stu-id="2b065-152">Managed identities are only available on resources running in an Azure cloud.</span></span>

<span data-ttu-id="2b065-153">В этом примере для подключения используется управляемое удостоверение среды узла.</span><span class="sxs-lookup"><span data-stu-id="2b065-153">This example connects using the managed identity of the host environment.</span></span> <span data-ttu-id="2b065-154">Например, при выполнении в VirtualMachine с назначенным Управляемым удостоверением службы код может обеспечивать вход с помощью назначенного удостоверения.</span><span class="sxs-lookup"><span data-stu-id="2b065-154">For example, if executed on a VirtualMachine with an assigned Managed Service Identity, this allows the code to sign in using that assigned identity.</span></span>

```azurepowershell-interactive
 Connect-AzAccount -Identity
```

## <a name="sign-in-with-a-non-default-tenant-or-as-a-cloud-solution-provider-csp"></a><span data-ttu-id="2b065-155">Вход с использованием нестандартного клиента или в качестве поставщика облачных решений (CSP)</span><span class="sxs-lookup"><span data-stu-id="2b065-155">Sign in with a non-default tenant or as a Cloud Solution Provider (CSP)</span></span>

<span data-ttu-id="2b065-156">Если ваша учетная запись связана с несколькими арендаторами, для входа требуется указать параметр `-Tenant` при подключении.</span><span class="sxs-lookup"><span data-stu-id="2b065-156">If your account is associated with more than one tenant, sign-in requires the `-Tenant` parameter to be specified when connecting.</span></span> <span data-ttu-id="2b065-157">Этот параметр работает с любым методом входа.</span><span class="sxs-lookup"><span data-stu-id="2b065-157">This parameter works with any sign-in method.</span></span> <span data-ttu-id="2b065-158">При входе в систему в качестве значения для этого параметра можно указать идентификатор объекта Azure клиента (идентификатор клиента) или полное доменное имя клиента.</span><span class="sxs-lookup"><span data-stu-id="2b065-158">When logging in, this parameter value can either be the Azure object ID of the tenant (Tenant ID) or the fully qualified domain name of the tenant.</span></span>

<span data-ttu-id="2b065-159">Если вы являетесь [поставщиком облачных решений](https://azure.microsoft.com/offers/ms-azr-0145p/), значением для `-Tenant`**должен** быть идентификатор клиента.</span><span class="sxs-lookup"><span data-stu-id="2b065-159">If you're a [Cloud Solution Provider (CSP)](https://azure.microsoft.com/offers/ms-azr-0145p/), the `-Tenant` value **must** be a tenant ID.</span></span>

```azurepowershell-interactive
Connect-AzAccount -Tenant 'xxxx-xxxx-xxxx-xxxx'
```

## <a name="sign-in-to-another-cloud"></a><span data-ttu-id="2b065-160">Вход в другое облако</span><span class="sxs-lookup"><span data-stu-id="2b065-160">Sign in to another Cloud</span></span>

<span data-ttu-id="2b065-161">Облачные службы Azure предоставляют среды, которые соответствуют региональным законам об обработке данных.</span><span class="sxs-lookup"><span data-stu-id="2b065-161">Azure cloud services offer environments compliant with regional data-handling laws.</span></span> <span data-ttu-id="2b065-162">Для учетных записей в региональном облаке нужно при входе указать среду с помощью аргумента `-Environment`.</span><span class="sxs-lookup"><span data-stu-id="2b065-162">For accounts in a regional cloud, set the environment when you sign in with the `-Environment` argument.</span></span> <span data-ttu-id="2b065-163">Этот параметр работает с любым методом входа.</span><span class="sxs-lookup"><span data-stu-id="2b065-163">This parameter works with any sign-in method.</span></span> <span data-ttu-id="2b065-164">Например, если ваша учетная запись находится в облаке для Китая, укажите следующее:</span><span class="sxs-lookup"><span data-stu-id="2b065-164">For example, if your account is in the China cloud:</span></span>

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

<span data-ttu-id="2b065-165">Следующая команда позволяет получить список доступных сред:</span><span class="sxs-lookup"><span data-stu-id="2b065-165">The following command gets a list of available environments:</span></span>

```azurepowershell-interactive
Get-AzEnvironment | Select-Object -Property Name
```
