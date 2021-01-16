---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/connect-azaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Connect-AzAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Connect-AzAccount.md
ms.openlocfilehash: e997013eb5646ca0f22904dd6fc68cf09a3ba228
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98393295"
---
# <span data-ttu-id="c04ed-101">Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="c04ed-101">Connect-AzAccount</span></span>

## <span data-ttu-id="c04ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c04ed-102">SYNOPSIS</span></span>
<span data-ttu-id="c04ed-103">Подключайтесь к Azure с помощью учетной записи, авторизированной для использования с командлетами из модулей Az PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c04ed-103">Connect to Azure with an authenticated account for use with cmdlets from the Az PowerShell modules.</span></span>

## <span data-ttu-id="c04ed-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c04ed-104">SYNTAX</span></span>

### <span data-ttu-id="c04ed-105">UserWithSubscriptionId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c04ed-105">UserWithSubscriptionId (Default)</span></span>
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] [-Subscription <String>] [-ContextName <String>]
 [-SkipContextPopulation] [-MaxContextPopulation <Int32>] [-UseDeviceAuthentication] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c04ed-106">ServicePrincipalWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c04ed-106">ServicePrincipalWithSubscriptionId</span></span>
```
Connect-AzAccount [-Environment <String>] -Credential <PSCredential> [-ServicePrincipal] -Tenant <String>
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-MaxContextPopulation <Int32>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c04ed-107">UserWithCredential</span><span class="sxs-lookup"><span data-stu-id="c04ed-107">UserWithCredential</span></span>
```
Connect-AzAccount [-Environment <String>] -Credential <PSCredential> [-Tenant <String>]
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-MaxContextPopulation <Int32>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c04ed-108">ServicePrincipalCertificateWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c04ed-108">ServicePrincipalCertificateWithSubscriptionId</span></span>
```
Connect-AzAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -Tenant <String> [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation]
 [-MaxContextPopulation <Int32>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c04ed-109">AccessTokenWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c04ed-109">AccessTokenWithSubscriptionId</span></span>
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] -AccessToken <String> [-GraphAccessToken <String>]
 [-KeyVaultAccessToken <String>] -AccountId <String> [-Subscription <String>] [-ContextName <String>]
 [-SkipValidation] [-SkipContextPopulation] [-MaxContextPopulation <Int32>] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c04ed-110">ManagedServiceLogin</span><span class="sxs-lookup"><span data-stu-id="c04ed-110">ManagedServiceLogin</span></span>
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] [-AccountId <String>] [-Identity]
 [-ManagedServicePort <Int32>] [-ManagedServiceHostName <String>] [-ManagedServiceSecret <SecureString>]
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-MaxContextPopulation <Int32>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c04ed-111">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c04ed-111">DESCRIPTION</span></span>

<span data-ttu-id="c04ed-112">Командлет подключается к Azure с помощью учетной записи, аутентификации для использования с командлетами из модулей `Connect-AzAccount` Az PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c04ed-112">The `Connect-AzAccount` cmdlet connects to Azure with an authenticated account for use with cmdlets from the Az PowerShell modules.</span></span> <span data-ttu-id="c04ed-113">Эту учетную запись, аутентификацию, можно использовать только с запросами Диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="c04ed-113">You can use this authenticated account only with Azure Resource Manager requests.</span></span> <span data-ttu-id="c04ed-114">Чтобы добавить учетную запись, предназначенную для использования с управлением службами, используйте `Add-AzureAccount` командлет из модуля Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c04ed-114">To add an authenticated account for use with Service Management, use the `Add-AzureAccount` cmdlet from the Azure PowerShell module.</span></span> <span data-ttu-id="c04ed-115">Если контекст для текущего пользователя не найден, его контекстный список заполняется контекстом для каждой из первых 25 подписок.</span><span class="sxs-lookup"><span data-stu-id="c04ed-115">If no context is found for the current user, the user's context list is populated with a context for each of their first 25 subscriptions.</span></span>
<span data-ttu-id="c04ed-116">Список контекстов, созданных для пользователя, можно найти с помощью `Get-AzContext -ListAvailable` запуска.</span><span class="sxs-lookup"><span data-stu-id="c04ed-116">The list of contexts created for the user can be found by running `Get-AzContext -ListAvailable`.</span></span> <span data-ttu-id="c04ed-117">Чтобы пропустить эту группу контекстов, укажите параметр **Switch Switch SkipContextPopulation.**</span><span class="sxs-lookup"><span data-stu-id="c04ed-117">To skip this context population, specify the **SkipContextPopulation** switch parameter.</span></span> <span data-ttu-id="c04ed-118">После выполнения этого cmdlet вы можете отключиться от учетной записи Azure с `Disconnect-AzAccount` помощью.</span><span class="sxs-lookup"><span data-stu-id="c04ed-118">After executing this cmdlet, you can disconnect from an Azure account using `Disconnect-AzAccount`.</span></span>

## <span data-ttu-id="c04ed-119">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c04ed-119">EXAMPLES</span></span>

### <span data-ttu-id="c04ed-120">Пример 1. Подключение к учетной записи Azure</span><span class="sxs-lookup"><span data-stu-id="c04ed-120">Example 1: Connect to an Azure account</span></span>

<span data-ttu-id="c04ed-121">В этом примере подключение к учетной записи Azure.</span><span class="sxs-lookup"><span data-stu-id="c04ed-121">This example connects to an Azure account.</span></span> <span data-ttu-id="c04ed-122">Необходимо предоставить учетную запись Майкрософт или учетные данные организации.</span><span class="sxs-lookup"><span data-stu-id="c04ed-122">You must provide a Microsoft account or organizational ID credentials.</span></span> <span data-ttu-id="c04ed-123">Если для ваших учетных данных включена многофакторная проверка подлинности, необходимо войти в систему с помощью интерактивного параметра или использовать проверку подлинности, главную службу.</span><span class="sxs-lookup"><span data-stu-id="c04ed-123">If multi-factor authentication is enabled for your credentials, you must log in using the interactive option or use service principal authentication.</span></span>

```powershell
Connect-AzAccount
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="c04ed-124">Пример 2. (Windows PowerShell 5.1) Подключение к Azure с помощью учетных данных удостоверений организации</span><span class="sxs-lookup"><span data-stu-id="c04ed-124">Example 2: (Windows PowerShell 5.1 only) Connect to Azure using organizational ID credentials</span></span>

<span data-ttu-id="c04ed-125">Этот сценарий работает только в Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="c04ed-125">This scenario works only in Windows PowerShell 5.1.</span></span> <span data-ttu-id="c04ed-126">Первая команда запросит учетные данные пользователей и сохраняет их в `$Credential` переменной.</span><span class="sxs-lookup"><span data-stu-id="c04ed-126">The first command prompts for user credentials and stores them in the `$Credential` variable.</span></span> <span data-ttu-id="c04ed-127">Вторая команда подключается к учетной записи Azure, используя учетные данные, хранимые в `$Credential` службе.</span><span class="sxs-lookup"><span data-stu-id="c04ed-127">The second command connects to an Azure account using the credentials stored in `$Credential`.</span></span> <span data-ttu-id="c04ed-128">Эта учетная запись аутентификация в Azure с использованием учетных данных организации.</span><span class="sxs-lookup"><span data-stu-id="c04ed-128">This account authenticates with Azure using organizational ID credentials.</span></span>

```powershell
$Credential = Get-Credential
Connect-AzAccount -Credential $Credential
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="c04ed-129">Пример 3. Подключение к Azure с помощью учетной записи основной службы</span><span class="sxs-lookup"><span data-stu-id="c04ed-129">Example 3: Connect to Azure using a service principal account</span></span>

<span data-ttu-id="c04ed-130">Первая команда запросит учетные данные для основной службы и сохраняет их в `$Credential` переменной.</span><span class="sxs-lookup"><span data-stu-id="c04ed-130">The first command prompts for service principal credentials and stores them in the `$Credential` variable.</span></span> <span data-ttu-id="c04ed-131">При запросе введите свой ИД приложения в качестве пароля для имени пользователя и секретного секрета службы.</span><span class="sxs-lookup"><span data-stu-id="c04ed-131">Enter your application ID for the username and service principal secret as the password when prompted.</span></span> <span data-ttu-id="c04ed-132">Вторая команда подключает указанный клиент Azure, используя учетные данные основной службы, хранимые в `$Credential` переменной.</span><span class="sxs-lookup"><span data-stu-id="c04ed-132">The second command connects the specified Azure tenant using the service principal credentials stored in the `$Credential` variable.</span></span> <span data-ttu-id="c04ed-133">Параметр **ServicePrincipal** switch указывает на то, что учетная запись является основной.</span><span class="sxs-lookup"><span data-stu-id="c04ed-133">The **ServicePrincipal** switch parameter indicates that the account authenticates as a service principal.</span></span>

```powershell
$Credential = Get-Credential
Connect-AzAccount -Credential $Credential -Tenant 'xxxx-xxxx-xxxx-xxxx' -ServicePrincipal
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
xxxx-xxxx-xxxx-xxxx    Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="c04ed-134">Пример 4. Использование интерактивного входа для подключения к определенному клиенту и подписке</span><span class="sxs-lookup"><span data-stu-id="c04ed-134">Example 4: Use an interactive login to connect to a specific tenant and subscription</span></span>

<span data-ttu-id="c04ed-135">В этом примере подключение к учетной записи Azure с указанным клиентом и подпиской.</span><span class="sxs-lookup"><span data-stu-id="c04ed-135">This example connects to an Azure account with the specified tenant and subscription.</span></span>

```powershell
Connect-AzAccount -Tenant 'xxxx-xxxx-xxxx-xxxx' -SubscriptionId 'yyyy-yyyy-yyyy-yyyy'
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="c04ed-136">Пример 5. Подключение с помощью удостоверения управляемой службы</span><span class="sxs-lookup"><span data-stu-id="c04ed-136">Example 5: Connect using a Managed Service Identity</span></span>

<span data-ttu-id="c04ed-137">Этот пример подключается с помощью MSI-удостоверения управляемой службы в среде хост-среды.</span><span class="sxs-lookup"><span data-stu-id="c04ed-137">This example connects using the Managed Service Identity (MSI) of the host environment.</span></span> <span data-ttu-id="c04ed-138">Например, вы можете войти в Azure с виртуальной машины, которая имеет назначенную MSI-запись.</span><span class="sxs-lookup"><span data-stu-id="c04ed-138">For example, you sign into Azure from a virtual machine that has an assigned MSI.</span></span>

```powershell
Connect-AzAccount -Identity
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
MSI@50342              Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="c04ed-139">Пример 6. Подключение с помощью учетных данных управляемых служб и ClientId</span><span class="sxs-lookup"><span data-stu-id="c04ed-139">Example 6: Connect using Managed Service Identity login and ClientId</span></span>

<span data-ttu-id="c04ed-140">В этом примере используется управляемое удостоверение **службы myUserAssignedIdentity.**</span><span class="sxs-lookup"><span data-stu-id="c04ed-140">This example connects using the Managed Service Identity of **myUserAssignedIdentity**.</span></span> <span data-ttu-id="c04ed-141">Он добавляет удостоверение пользователя, назначенное пользователю, на виртуальную машину, а затем подключается с помощью идентификатора ClientId пользователя.</span><span class="sxs-lookup"><span data-stu-id="c04ed-141">It adds the user assigned identity to the virtual machine, then connects using the ClientId of the user assigned identity.</span></span> <span data-ttu-id="c04ed-142">Дополнительные сведения см. в [сведениях о настройке управляемых удостоверений для ресурсов Azure на VM-клиенте Azure.](/azure/active-directory/managed-identities-azure-resources/qs-configure-powershell-windows-vm)</span><span class="sxs-lookup"><span data-stu-id="c04ed-142">For more information, see [Configure managed identities for Azure resources on an Azure VM](/azure/active-directory/managed-identities-azure-resources/qs-configure-powershell-windows-vm).</span></span>

```powershell
$identity = Get-AzUserAssignedIdentity -ResourceGroupName 'myResourceGroup' -Name 'myUserAssignedIdentity'
Get-AzVM -ResourceGroupName contoso -Name testvm | Update-AzVM -IdentityType UserAssigned -IdentityId $identity.Id
Connect-AzAccount -Identity -AccountId $identity.ClientId # Run on the virtual machine
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
yyyy-yyyy-yyyy-yyyy    Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="c04ed-143">Пример 7. Подключение с помощью сертификатов</span><span class="sxs-lookup"><span data-stu-id="c04ed-143">Example 7: Connect using certificates</span></span>

<span data-ttu-id="c04ed-144">В этом примере подключение к учетной записи Azure с помощью проверки подлинности на основе сертификата.</span><span class="sxs-lookup"><span data-stu-id="c04ed-144">This example connects to an Azure account using certificate-based service principal authentication.</span></span>
<span data-ttu-id="c04ed-145">Необходимо создать главную службу проверки подлинности с помощью указанного сертификата.</span><span class="sxs-lookup"><span data-stu-id="c04ed-145">The service principal used for authentication must be created with the specified certificate.</span></span> <span data-ttu-id="c04ed-146">Дополнительные сведения о создании самозаверяющих сертификатов и назначении им разрешений см. в справке Azure PowerShell для создания основной службы с [помощью сертификата.](/azure/active-directory/develop/howto-authenticate-service-principal-powershell)</span><span class="sxs-lookup"><span data-stu-id="c04ed-146">For more information on creating a self-signed certificates and assigning them permissions, see [Use Azure PowerShell to create a service principal with a certificate](/azure/active-directory/develop/howto-authenticate-service-principal-powershell)</span></span>

```powershell
$Thumbprint = '0SZTNJ34TCCMUJ5MJZGR8XQD3S0RVHJBA33Z8ZXV'
$TenantId = '4cd76576-b611-43d0-8f2b-adcb139531bf'
$ApplicationId = '3794a65a-e4e4-493d-ac1d-f04308d712dd'
Connect-AzAccount -CertificateThumbprint $Thumbprint -ApplicationId $ApplicationId -Tenant $TenantId -ServicePrincipal
```

```Output
Account             SubscriptionName TenantId            Environment
-------             ---------------- --------            -----------
xxxx-xxxx-xxxx-xxxx Subscription1    xxxx-xxxx-xxxx-xxxx AzureCloud

Account          : 3794a65a-e4e4-493d-ac1d-f04308d712dd
SubscriptionName : MyTestSubscription
SubscriptionId   : 85f0f653-1f86-4d2c-a9f1-042efc00085c
TenantId         : 4cd76576-b611-43d0-8f2b-adcb139531bf
Environment      : AzureCloud
```

## <span data-ttu-id="c04ed-147">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c04ed-147">PARAMETERS</span></span>

### <span data-ttu-id="c04ed-148">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="c04ed-148">-AccessToken</span></span>

<span data-ttu-id="c04ed-149">Определяет маркер доступа.</span><span class="sxs-lookup"><span data-stu-id="c04ed-149">Specifies an access token.</span></span>

> [!CAUTION]
> <span data-ttu-id="c04ed-150">Маркеры доступа — это тип учетных данных.</span><span class="sxs-lookup"><span data-stu-id="c04ed-150">Access tokens are a type of credential.</span></span> <span data-ttu-id="c04ed-151">Для сохранения конфиденциальной информации необходимо принять соответствующие меры безопасности.</span><span class="sxs-lookup"><span data-stu-id="c04ed-151">You should take the appropriate security precautions to keep them confidential.</span></span> <span data-ttu-id="c04ed-152">Маркеры доступа также имеют время выполнения и могут препятствовать выполнению длинных задач.</span><span class="sxs-lookup"><span data-stu-id="c04ed-152">Access tokens also timeout and may prevent long running tasks from completing.</span></span>

```yaml
Type: System.String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c04ed-153">-AccountId</span><span class="sxs-lookup"><span data-stu-id="c04ed-153">-AccountId</span></span>

<span data-ttu-id="c04ed-154">ИД учетной записи для маркера доступа в **наборе параметров AccessToken.**</span><span class="sxs-lookup"><span data-stu-id="c04ed-154">Account ID for access token in **AccessToken** parameter set.</span></span> <span data-ttu-id="c04ed-155">ИД учетной записи для управляемой службы в наборе параметров **ManagedService.**</span><span class="sxs-lookup"><span data-stu-id="c04ed-155">Account ID for managed service in **ManagedService** parameter set.</span></span> <span data-ttu-id="c04ed-156">Может быть управляемым ИД ресурса службы или связанным с ним ид клиента.</span><span class="sxs-lookup"><span data-stu-id="c04ed-156">Can be a managed service resource ID, or the associated client ID.</span></span>
<span data-ttu-id="c04ed-157">Чтобы использовать назначенное системой удостоверение, оставьте это поле пустым.</span><span class="sxs-lookup"><span data-stu-id="c04ed-157">To use the system assigned identity, leave this field blank.</span></span>

```yaml
Type: System.String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ManagedServiceLogin
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c04ed-158">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="c04ed-158">-ApplicationId</span></span>

<span data-ttu-id="c04ed-159">ИД приложения для основной услуги.</span><span class="sxs-lookup"><span data-stu-id="c04ed-159">Application ID of the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c04ed-160">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="c04ed-160">-CertificateThumbprint</span></span>

<span data-ttu-id="c04ed-161">"Hash" (Hash) сертификата или Thumbprint.</span><span class="sxs-lookup"><span data-stu-id="c04ed-161">Certificate Hash or Thumbprint.</span></span>

```yaml
Type: System.String
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c04ed-162">-ContextName</span><span class="sxs-lookup"><span data-stu-id="c04ed-162">-ContextName</span></span>

<span data-ttu-id="c04ed-163">Имя контекста Azure по умолчанию для этого входа.</span><span class="sxs-lookup"><span data-stu-id="c04ed-163">Name of the default Azure context for this login.</span></span> <span data-ttu-id="c04ed-164">Дополнительные сведения о контекстах Azure см. в контекстных объектах [Azure PowerShell.](/powershell/azure/context-persistence)</span><span class="sxs-lookup"><span data-stu-id="c04ed-164">For more information about Azure contexts, see [Azure PowerShell context objects](/powershell/azure/context-persistence).</span></span>

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

### <span data-ttu-id="c04ed-165">-Credential</span><span class="sxs-lookup"><span data-stu-id="c04ed-165">-Credential</span></span>

<span data-ttu-id="c04ed-166">Указывает объект **PSCredential.**</span><span class="sxs-lookup"><span data-stu-id="c04ed-166">Specifies a **PSCredential** object.</span></span> <span data-ttu-id="c04ed-167">Чтобы получить дополнительные сведения о **объекте PSCredential,** введите `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="c04ed-167">For more information about the **PSCredential** object, type `Get-Help Get-Credential`.</span></span> <span data-ttu-id="c04ed-168">Объект **PSCredential** предоставляет ИД пользователя и пароль для учетных данных организации, а также код приложения и секрет для учетных данных директора-службы.</span><span class="sxs-lookup"><span data-stu-id="c04ed-168">The **PSCredential** object provides the user ID and password for organizational ID credentials, or the application ID and secret for service principal credentials.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: ServicePrincipalWithSubscriptionId, UserWithCredential
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c04ed-169">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c04ed-169">-DefaultProfile</span></span>

<span data-ttu-id="c04ed-170">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c04ed-170">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c04ed-171">-Среда</span><span class="sxs-lookup"><span data-stu-id="c04ed-171">-Environment</span></span>

<span data-ttu-id="c04ed-172">Среда, содержащая учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="c04ed-172">Environment containing the Azure account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EnvironmentName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c04ed-173">-Force</span><span class="sxs-lookup"><span data-stu-id="c04ed-173">-Force</span></span>

<span data-ttu-id="c04ed-174">Переописывание существующего контекста с тем же именем без запроса.</span><span class="sxs-lookup"><span data-stu-id="c04ed-174">Overwrite the existing context with the same name without prompting.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c04ed-175">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="c04ed-175">-GraphAccessToken</span></span>

<span data-ttu-id="c04ed-176">AccessToken для службы Graph.</span><span class="sxs-lookup"><span data-stu-id="c04ed-176">AccessToken for Graph Service.</span></span>

```yaml
Type: System.String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c04ed-177">-Identity</span><span class="sxs-lookup"><span data-stu-id="c04ed-177">-Identity</span></span>

<span data-ttu-id="c04ed-178">Вход с использованием удостоверения управляемой службы.</span><span class="sxs-lookup"><span data-stu-id="c04ed-178">Login using a Managed Service Identity.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ManagedServiceLogin
Aliases: MSI, ManagedService

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c04ed-179">-KeyVaultAccessToken</span><span class="sxs-lookup"><span data-stu-id="c04ed-179">-KeyVaultAccessToken</span></span>

<span data-ttu-id="c04ed-180">AccessToken для службы KeyVault.</span><span class="sxs-lookup"><span data-stu-id="c04ed-180">AccessToken for KeyVault Service.</span></span>

```yaml
Type: System.String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c04ed-181">-ManagedServiceHostName</span><span class="sxs-lookup"><span data-stu-id="c04ed-181">-ManagedServiceHostName</span></span>

<span data-ttu-id="c04ed-182">Устарело.</span><span class="sxs-lookup"><span data-stu-id="c04ed-182">Obsolete.</span></span> <span data-ttu-id="c04ed-183">Чтобы использовать настраиваемую конечную точку MSI, заняйте переменную среды MSI_ENDPOINT, например" http://localhost:50342/oauth2/token ".</span><span class="sxs-lookup"><span data-stu-id="c04ed-183">To use customized MSI endpoint, please set environment variable MSI_ENDPOINT, e.g. "http://localhost:50342/oauth2/token".</span></span> <span data-ttu-id="c04ed-184">Имя хоста управляемой службы.</span><span class="sxs-lookup"><span data-stu-id="c04ed-184">Host name for the managed service.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagedServiceLogin
Aliases:

Required: False
Position: Named
Default value: localhost
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c04ed-185">-ManagedServicePort</span><span class="sxs-lookup"><span data-stu-id="c04ed-185">-ManagedServicePort</span></span>

<span data-ttu-id="c04ed-186">Устарело.</span><span class="sxs-lookup"><span data-stu-id="c04ed-186">Obsolete.</span></span> <span data-ttu-id="c04ed-187">Чтобы использовать настраиваемую конечную точку MSI, заняйте переменную среды MSI_ENDPOINT, например" http://localhost:50342/oauth2/token ". Номер порта для управляемой службы.</span><span class="sxs-lookup"><span data-stu-id="c04ed-187">To use customized MSI endpoint, please set environment variable MSI_ENDPOINT, e.g. "http://localhost:50342/oauth2/token".Port number for the managed service.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ManagedServiceLogin
Aliases:

Required: False
Position: Named
Default value: 50342
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c04ed-188">-ManagedServiceSecret</span><span class="sxs-lookup"><span data-stu-id="c04ed-188">-ManagedServiceSecret</span></span>

<span data-ttu-id="c04ed-189">Устарело.</span><span class="sxs-lookup"><span data-stu-id="c04ed-189">Obsolete.</span></span> <span data-ttu-id="c04ed-190">Чтобы использовать настраиваемый секрет MSI, зайте параметры переменной среды MSI_SECRET.</span><span class="sxs-lookup"><span data-stu-id="c04ed-190">To use customized MSI secret, please set environment variable MSI_SECRET.</span></span> <span data-ttu-id="c04ed-191">Маркер для входа в управляемые службы.</span><span class="sxs-lookup"><span data-stu-id="c04ed-191">Token for the managed service login.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ManagedServiceLogin
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c04ed-192">-MaxContextPopulation</span><span class="sxs-lookup"><span data-stu-id="c04ed-192">-MaxContextPopulation</span></span>

<span data-ttu-id="c04ed-193">Максимальный номер подписки для заполнения контекстов после входа.</span><span class="sxs-lookup"><span data-stu-id="c04ed-193">Max subscription number to populate contexts after login.</span></span> <span data-ttu-id="c04ed-194">Значение по умолчанию — 25.</span><span class="sxs-lookup"><span data-stu-id="c04ed-194">Default is 25.</span></span> <span data-ttu-id="c04ed-195">Чтобы заполнить все подписки контекстами, установите -1.</span><span class="sxs-lookup"><span data-stu-id="c04ed-195">To populate all subscriptions to contexts, set to -1.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c04ed-196">-Scope</span><span class="sxs-lookup"><span data-stu-id="c04ed-196">-Scope</span></span>

<span data-ttu-id="c04ed-197">Определяет область изменения контекста, например, применяются ли изменения только к текущему процессу или же к всем сеансам, на которые начал пользователь.</span><span class="sxs-lookup"><span data-stu-id="c04ed-197">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c04ed-198">-ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="c04ed-198">-ServicePrincipal</span></span>

<span data-ttu-id="c04ed-199">Указывает на то, что эта учетная запись аутентификация путем предоставления учетных данных для основной службы.</span><span class="sxs-lookup"><span data-stu-id="c04ed-199">Indicates that this account authenticates by providing service principal credentials.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServicePrincipalWithSubscriptionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c04ed-200">-SkipContextPopulation</span><span class="sxs-lookup"><span data-stu-id="c04ed-200">-SkipContextPopulation</span></span>

<span data-ttu-id="c04ed-201">Пропускает контекстную группу, если контексты не найдены.</span><span class="sxs-lookup"><span data-stu-id="c04ed-201">Skips context population if no contexts are found.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c04ed-202">-SkipValidation</span><span class="sxs-lookup"><span data-stu-id="c04ed-202">-SkipValidation</span></span>

<span data-ttu-id="c04ed-203">Пропустить проверку для маркера доступа.</span><span class="sxs-lookup"><span data-stu-id="c04ed-203">Skip validation for access token.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AccessTokenWithSubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c04ed-204">-Подписка</span><span class="sxs-lookup"><span data-stu-id="c04ed-204">-Subscription</span></span>

<span data-ttu-id="c04ed-205">Имя или ИД подписки.</span><span class="sxs-lookup"><span data-stu-id="c04ed-205">Subscription Name or ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName, SubscriptionId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c04ed-206">-Tenant</span><span class="sxs-lookup"><span data-stu-id="c04ed-206">-Tenant</span></span>

<span data-ttu-id="c04ed-207">Необязательное имя клиента или ИД.</span><span class="sxs-lookup"><span data-stu-id="c04ed-207">Optional tenant name or ID.</span></span>

> [!NOTE]
> <span data-ttu-id="c04ed-208">Из-за ограничений текущего API при подключении с учетной записью "бизнес-бизнес" необходимо использовать вместо имени клиента ИД клиента.</span><span class="sxs-lookup"><span data-stu-id="c04ed-208">Due to limitations of the current API, you must use a tenant ID instead of a tenant name when connecting with a business-to-business (B2B) account.</span></span>

```yaml
Type: System.String
Parameter Sets: UserWithSubscriptionId, UserWithCredential, AccessTokenWithSubscriptionId, ManagedServiceLogin
Aliases: Domain, TenantId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ServicePrincipalWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionId
Aliases: Domain, TenantId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c04ed-209">-UseDeviceAuthentication</span><span class="sxs-lookup"><span data-stu-id="c04ed-209">-UseDeviceAuthentication</span></span>

<span data-ttu-id="c04ed-210">Используйте проверку подлинности кода устройства вместо управления браузером.</span><span class="sxs-lookup"><span data-stu-id="c04ed-210">Use device code authentication instead of a browser control.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UserWithSubscriptionId
Aliases: DeviceCode, DeviceAuth, Device

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c04ed-211">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c04ed-211">-Confirm</span></span>

<span data-ttu-id="c04ed-212">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="c04ed-212">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c04ed-213">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c04ed-213">-WhatIf</span></span>

<span data-ttu-id="c04ed-214">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c04ed-214">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c04ed-215">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c04ed-215">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c04ed-216">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c04ed-216">CommonParameters</span></span>
<span data-ttu-id="c04ed-217">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c04ed-217">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c04ed-218">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c04ed-218">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c04ed-219">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c04ed-219">INPUTS</span></span>

### <span data-ttu-id="c04ed-220">System.String</span><span class="sxs-lookup"><span data-stu-id="c04ed-220">System.String</span></span>

## <span data-ttu-id="c04ed-221">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c04ed-221">OUTPUTS</span></span>

### <span data-ttu-id="c04ed-222">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="c04ed-222">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile</span></span>

## <span data-ttu-id="c04ed-223">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c04ed-223">NOTES</span></span>

## <span data-ttu-id="c04ed-224">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c04ed-224">RELATED LINKS</span></span>
