---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/connect-azaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Connect-AzAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Connect-AzAccount.md
ms.openlocfilehash: 87e8615e7862e8b3314c9dace4849621a8ed4c78
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909450"
---
# <span data-ttu-id="ff93f-101">Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="ff93f-101">Connect-AzAccount</span></span>

## <span data-ttu-id="ff93f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ff93f-102">SYNOPSIS</span></span>
<span data-ttu-id="ff93f-103">Подключитесь к Azure с учетной записью, прошедшим проверку подлинности, для использования с запросом командлетов Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="ff93f-103">Connect to Azure with an authenticated account for use with Azure Resource Manager cmdlet requests.</span></span>

## <span data-ttu-id="ff93f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ff93f-104">SYNTAX</span></span>

### <span data-ttu-id="ff93f-105">UserWithSubscriptionId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ff93f-105">UserWithSubscriptionId (Default)</span></span>
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] [-Subscription <String>] [-ContextName <String>]
 [-SkipContextPopulation] [-UseDeviceAuthentication] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff93f-106">ServicePrincipalWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ff93f-106">ServicePrincipalWithSubscriptionId</span></span>
```
Connect-AzAccount [-Environment <String>] -Credential <PSCredential> [-ServicePrincipal] -Tenant <String>
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ff93f-107">UserWithCredential</span><span class="sxs-lookup"><span data-stu-id="ff93f-107">UserWithCredential</span></span>
```
Connect-AzAccount [-Environment <String>] -Credential <PSCredential> [-Tenant <String>]
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ff93f-108">ServicePrincipalCertificateWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ff93f-108">ServicePrincipalCertificateWithSubscriptionId</span></span>
```
Connect-AzAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -Tenant <String> [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ff93f-109">AccessTokenWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ff93f-109">AccessTokenWithSubscriptionId</span></span>
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] -AccessToken <String> [-GraphAccessToken <String>]
 [-KeyVaultAccessToken <String>] -AccountId <String> [-Subscription <String>] [-ContextName <String>]
 [-SkipValidation] [-SkipContextPopulation] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff93f-110">ManagedServiceLogin</span><span class="sxs-lookup"><span data-stu-id="ff93f-110">ManagedServiceLogin</span></span>
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] [-AccountId <String>] [-Identity]
 [-ManagedServicePort <Int32>] [-ManagedServiceHostName <String>] [-ManagedServiceSecret <SecureString>]
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ff93f-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ff93f-111">DESCRIPTION</span></span>
<span data-ttu-id="ff93f-112">Командлет Connect-AzAccount подключает к Azure учетную запись с проверкой подлинности для использования с запросом командлета диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="ff93f-112">The Connect-AzAccount cmdlet connects to Azure with an authenticated account for use with Azure Resource Manager cmdlet requests.</span></span>
<span data-ttu-id="ff93f-113">Вы можете использовать эту учетную запись с проверкой подлинности только для командлетов Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="ff93f-113">You can use this authenticated account only with Azure Resource Manager cmdlets.</span></span>
<span data-ttu-id="ff93f-114">Чтобы добавить учетную запись, прошедший проверку подлинности, с помощью командлетов управления службами, используйте Add-AzAccount или Import-AzPublishSettingsFile.</span><span class="sxs-lookup"><span data-stu-id="ff93f-114">To add an authenticated account for use with Service Management cmdlets, use the Add-AzAccount or the Import-AzPublishSettingsFile cmdlet.</span></span>
<span data-ttu-id="ff93f-115">Если для текущего пользователя контекст не найден, эта команда заполнит список контекста пользователя, указав контекст для каждой из подписок (первых 25).</span><span class="sxs-lookup"><span data-stu-id="ff93f-115">If no context is found for the current user, this command will populate the user's context list with a context for each of their (first 25) subscriptions.</span></span> <span data-ttu-id="ff93f-116">Список контекстов, созданных для пользователя, можно найти, выполнив "Get-AzContext-ListAvailable".</span><span class="sxs-lookup"><span data-stu-id="ff93f-116">The list of contexts created for the user can be found by running "Get-AzContext -ListAvailable".</span></span> <span data-ttu-id="ff93f-117">Чтобы пропустить это заполнение, вы можете выполнить эту команду с параметром "-SkipContextPopulation".</span><span class="sxs-lookup"><span data-stu-id="ff93f-117">To skip this context population, you can run this command with the "-SkipContextPopulation" switch parameter.</span></span>
<span data-ttu-id="ff93f-118">После выполнения этого командлета вы можете отключиться от учетной записи Azure с помощью команды Disconnect-AzAccount.</span><span class="sxs-lookup"><span data-stu-id="ff93f-118">After executing this cmdlet, you can disconnect from an Azure account using Disconnect-AzAccount.</span></span>

## <span data-ttu-id="ff93f-119">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ff93f-119">EXAMPLES</span></span>

### <span data-ttu-id="ff93f-120">Пример 1: использование интерактивного входа для подключения к учетной записи Azure</span><span class="sxs-lookup"><span data-stu-id="ff93f-120">Example 1: Use an interactive login to connect to an Azure account</span></span>
```powershell
PS C:\> Connect-AzAccount

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="ff93f-121">Эта команда соединяется с учетной записью Azure.</span><span class="sxs-lookup"><span data-stu-id="ff93f-121">This command connects to an Azure account.</span></span>
<span data-ttu-id="ff93f-122">Чтобы запустить командлеты диспетчера ресурсов Azure с этой учетной записью, необходимо задать учетные данные учетной записи Майкрософт или идентификатора организации в запросе.</span><span class="sxs-lookup"><span data-stu-id="ff93f-122">To run Azure Resource Manager cmdlets with this account, you must provide Microsoft account or organizational ID credentials at the prompt.</span></span>
<span data-ttu-id="ff93f-123">Если для ваших учетных данных включена многофакторная проверка подлинности, вы должны войти в систему с помощью интерактивного режима или воспользоваться проверкой подлинности субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="ff93f-123">If multi-factor authentication is enabled for your credentials, you must log in using the interactive option or use service principal authentication.</span></span>

### <span data-ttu-id="ff93f-124">Пример 2: (только для Windows PowerShell 5,1) подключение к учетной записи Azure с использованием учетных данных идентификатора Организации</span><span class="sxs-lookup"><span data-stu-id="ff93f-124">Example 2: (Windows PowerShell 5.1 only) Connect to an Azure account using organizational ID credentials</span></span>
```powershell
PS C:\> $Credential = Get-Credential
PS C:\> Connect-AzAccount -Credential $Credential

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="ff93f-125">Этот сценарий работает только в Windows PowerShell 5,1.</span><span class="sxs-lookup"><span data-stu-id="ff93f-125">This scenario works only in Windows PowerShell 5.1.</span></span> <span data-ttu-id="ff93f-126">Первая команда предложит ввести учетные данные пользователя (имя пользователя и пароль), а затем сохранит их в переменной $Credential.</span><span class="sxs-lookup"><span data-stu-id="ff93f-126">The first command will prompt for user credentials (username and password), and then stores them in the $Credential variable.</span></span>
<span data-ttu-id="ff93f-127">Вторая команда подключается к учетной записи Azure с использованием учетных данных, которые хранятся в $Credential.</span><span class="sxs-lookup"><span data-stu-id="ff93f-127">The second command connects to an Azure account using the credentials stored in $Credential.</span></span>
<span data-ttu-id="ff93f-128">Эта учетная запись проходит проверку подлинности с помощью диспетчера ресурсов Azure с использованием учетных данных идентификатора организации.</span><span class="sxs-lookup"><span data-stu-id="ff93f-128">This account authenticates with Azure Resource Manager using organizational ID credentials.</span></span>
<span data-ttu-id="ff93f-129">Для запуска командлетов диспетчера ресурсов Azure с этой учетной записью нельзя использовать многофакторную проверку подлинности или учетные данные учетной записи Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="ff93f-129">You cannot use multi-factor authentication or Microsoft account credentials to run Azure Resource Manager cmdlets with this account.</span></span>

### <span data-ttu-id="ff93f-130">Пример 3: подключение к учетной записи субъекта-службы Azure</span><span class="sxs-lookup"><span data-stu-id="ff93f-130">Example 3: Connect to an Azure service principal account</span></span>
```powershell
PS C:\> $Credential = Get-Credential
PS C:\> Connect-AzAccount -Credential $Credential -Tenant "xxxx-xxxx-xxxx-xxxx" -ServicePrincipal

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
xxxx-xxxx-xxxx-xxxx    Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="ff93f-131">Первая команда получает учетные данные субъекта-службы (идентификатор приложения и секретный ключ участника-службы), а затем сохраняет их в переменной $Credential.</span><span class="sxs-lookup"><span data-stu-id="ff93f-131">The first command gets the service principal credentials (application id and service principal secret), and then stores them in the $Credential variable.</span></span>
<span data-ttu-id="ff93f-132">Вторая команда подключается к Azure с использованием учетных данных субъекта-службы, хранящихся в $Credential для указанного клиента.</span><span class="sxs-lookup"><span data-stu-id="ff93f-132">The second command connect to Azure using the service principal credentials stored in $Credential for the specified Tenant.</span></span>
<span data-ttu-id="ff93f-133">Параметр ключа ServicePrincipal указывает, что учетная запись проходит проверку подлинности субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="ff93f-133">The ServicePrincipal switch parameter indicates that the account authenticates as a service principal.</span></span>

### <span data-ttu-id="ff93f-134">Пример 4: использование интерактивного входа для подключения к учетной записи для определенного клиента и подписки</span><span class="sxs-lookup"><span data-stu-id="ff93f-134">Example 4: Use an interactive login to connect to an account for a specific tenant and subscription</span></span>
```powershell
PS C:\> Connect-AzAccount -Tenant "xxxx-xxxx-xxxx-xxxx" -SubscriptionId "yyyy-yyyy-yyyy-yyyy"

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="ff93f-135">Эта команда соединяется с учетной записью Azure и настроила AzureRM PowerShell для запуска командлетов для указанного клиента и подписки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ff93f-135">This command connects to an Azure account and configured AzureRM PowerShell to run cmdlets for the specified tenant and subscription by default.</span></span>

### <span data-ttu-id="ff93f-136">Пример 5: Добавление учетной записи с помощью имени входа для удостоверения управляемой службы</span><span class="sxs-lookup"><span data-stu-id="ff93f-136">Example 5: Add an Account Using Managed Service Identity Login</span></span>
```powershell
PS C:\> Connect-AzAccount -Identity

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
MSI@50342              Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="ff93f-137">Эта команда соединяется с использованием управляемого удостоверения среды хоста (например, если выполняется в VirtualMachine с назначенным идентификатором управляемой службы, это позволит коду войти в систему с помощью этого назначенного удостоверения).</span><span class="sxs-lookup"><span data-stu-id="ff93f-137">This command connects using the managed service identity of the host environment (for example, if executed on a VirtualMachine with an assigned Managed Service Identity, this will allow the code to login using that assigned identity)</span></span>

### <span data-ttu-id="ff93f-138">Пример 6: Добавление учетной записи с использованием учетных данных для входа на управляемую службу и ClientId</span><span class="sxs-lookup"><span data-stu-id="ff93f-138">Example 6: Add an Account Using Managed Service Identity Login and ClientId</span></span>
```powershell
PS C:\> $identity = Get-AzUserAssignedIdentity -ResourceGroupName "myResourceGroup" -Name "myUserAssignedIdentity"
PS C:\> Get-AzVM -ResourceGroupName contoso -Name testvm | Update-AzVM -IdentityType UserAssigned -IdentityId $identity.Id
PS C:\> Connect-AzAccount -Identity -AccountId $identity.ClientId # Run on the "testvm" virtual machine

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
yyyy-yyyy-yyyy-yyyy    Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="ff93f-139">Эта команда соединяется с помощью удостоверения управляемой службы "myUserAssignedIdentity", добавив удостоверение пользователя для виртуальной машины, а затем подключив его с помощью ClientId идентификатора, назначенного пользователю.</span><span class="sxs-lookup"><span data-stu-id="ff93f-139">This command connects using the managed service identity of "myUserAssignedIdentity" by adding the User Assigned Identity to the Virtual Machine, then connecting using the ClientId of the User Assigned Identity.</span></span>
<span data-ttu-id="ff93f-140">Дополнительные сведения о настройке управляемых удостоверений можно найти здесь: https://docs.microsoft.com/en-us/azure/active-directory/managed-identities-azure-resources/qs-configure-powershell-windows-vm .</span><span class="sxs-lookup"><span data-stu-id="ff93f-140">More information about configuring Managed Identities can be found here: https://docs.microsoft.com/en-us/azure/active-directory/managed-identities-azure-resources/qs-configure-powershell-windows-vm.</span></span>

### <span data-ttu-id="ff93f-141">Пример 7: Добавление учетной записи с использованием учетных данных для входа на управляемую службу и ClientId</span><span class="sxs-lookup"><span data-stu-id="ff93f-141">Example 7: Add an Account Using Managed Service Identity Login and ClientId</span></span>
```powershell
PS C:\> $identity = Get-AzUserAssignedIdentity -ResourceGroupName "myResourceGroup" -Name "myUserAssignedIdentity"
PS C:\> Get-AzVM -ResourceGroupName contoso -Name testvm | Update-AzVM -IdentityType UserAssigned -IdentityId $identity.Id
PS C:\> Connect-AzAccount -Identity -AccountId $identity.Id # Run on the "testvm" virtual machine

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
yyyy-yyyy-yyyy-yyyy    Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="ff93f-142">Эта команда соединяется с помощью удостоверения управляемой службы "myUserAssignedIdentity", добавив удостоверение пользователя для виртуальной машины, а затем подключив его с помощью идентификатора пользователя, которому назначена идентификация.</span><span class="sxs-lookup"><span data-stu-id="ff93f-142">This command connects using the managed service identity of "myUserAssignedIdentity" by adding the User Assigned Identity to the Virtual Machine, then connecting using the Id of the User Assigned Identity.</span></span>
<span data-ttu-id="ff93f-143">Дополнительные сведения о настройке управляемых удостоверений можно найти здесь: https://docs.microsoft.com/en-us/azure/active-directory/managed-identities-azure-resources/qs-configure-powershell-windows-vm .</span><span class="sxs-lookup"><span data-stu-id="ff93f-143">More information about configuring Managed Identities can be found here: https://docs.microsoft.com/en-us/azure/active-directory/managed-identities-azure-resources/qs-configure-powershell-windows-vm.</span></span>

### <span data-ttu-id="ff93f-144">Пример 8: Добавление учетной записи с помощью сертификатов</span><span class="sxs-lookup"><span data-stu-id="ff93f-144">Example 8: Add an account using certificates</span></span>
```powershell
# For more information on creating a self-signed certificate
# and giving it proper permissions, please see the following:
# https://docs.microsoft.com/en-us/azure/active-directory/develop/howto-authenticate-service-principal-powershell
PS C:\> $Thumbprint = "0SZTNJ34TCCMUJ5MJZGR8XQD3S0RVHJBA33Z8ZXV"
PS C:\> $TenantId = "4cd76576-b611-43d0-8f2b-adcb139531bf"
PS C:\> $ApplicationId = "3794a65a-e4e4-493d-ac1d-f04308d712dd"
PS C:\> Connect-AzAccount -CertificateThumbprint $Thumbprint -ApplicationId $ApplicationId -Tenant $TenantId -ServicePrincipal

Account             SubscriptionName TenantId            Environment
-------             ---------------- --------            -----------
xxxx-xxxx-xxxx-xxxx Subscription1    xxxx-xxxx-xxxx-xxxx AzureCloud

Account          : 3794a65a-e4e4-493d-ac1d-f04308d712dd
SubscriptionName : MyTestSubscription
SubscriptionId   : 85f0f653-1f86-4d2c-a9f1-042efc00085c
TenantId         : 4cd76576-b611-43d0-8f2b-adcb139531bf
Environment      : AzureCloud
```

<span data-ttu-id="ff93f-145">Эта команда используется для подключения к учетной записи Azure с использованием проверки подлинности субъекта-службы на основе сертификатов.</span><span class="sxs-lookup"><span data-stu-id="ff93f-145">This command connects to an Azure account using certificate-based service principal authentication.</span></span> <span data-ttu-id="ff93f-146">Субъект-служба, используемая для проверки подлинности, должна быть создана с помощью данного сертификата.</span><span class="sxs-lookup"><span data-stu-id="ff93f-146">The service principal used for authentication should have been created with the given certificate.</span></span>

### <span data-ttu-id="ff93f-147">Пример 9: Добавление учетной записи с использованием проверки подлинности AccessToken</span><span class="sxs-lookup"><span data-stu-id="ff93f-147">Example 9: Add an account using AccessToken authentication</span></span>
```powershell
PS C:\> $url = "https://login.windows.net/<TenantId>/oauth2/token"
PS C:\> $body = "grant_type=refresh_token&refresh_token=<refreshtoken>" # Refresh token obtained from ~/.azure/TokenCache.dat
PS C:\> $response = Invoke-RestMethod $url -Method POST -Body $body
PS C:\> $AccessToken = $response.access_token
PS C:\> $body1 = $body + "&resource=https%3A%2F%2Fvault.azure.net"
PS C:\> $response = Invoke-RestMethod $url -Method POST -Body $body1
PS C:\> $body2 = $body + "&resource=https%3A%2F%2Fgraph.windows.net"
PS C:\> $GraphAccessToken = $response.access_token
PS C:\> Connect-AzAccount -AccountId "azureuser@contoso.com" -AccessToken $AccessToken -KeyVaultAccessToken $KeyVaultAccessToken -GraphAccessToken $GraphAccessToken -Tenant "xxxx-xxxx-xxxx-xxxx" -SubscriptionId "yyyy-yyyy-yyyy-yyyy"

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="ff93f-148">Эта команда соединяется с учетной записью Azure, указанной в поле AccountId, с использованием AccessToken и KeyVaultAccessToken.</span><span class="sxs-lookup"><span data-stu-id="ff93f-148">This command connects to an Azure account specified in "AccountId" using the AccessToken and KeyVaultAccessToken provided.</span></span>

## <span data-ttu-id="ff93f-149">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ff93f-149">PARAMETERS</span></span>

### <span data-ttu-id="ff93f-150">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="ff93f-150">-AccessToken</span></span>
<span data-ttu-id="ff93f-151">Задает маркер доступа.</span><span class="sxs-lookup"><span data-stu-id="ff93f-151">Specifies an access token.</span></span>

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

### <span data-ttu-id="ff93f-152">-AccountId</span><span class="sxs-lookup"><span data-stu-id="ff93f-152">-AccountId</span></span>
<span data-ttu-id="ff93f-153">Идентификатор учетной записи для маркера доступа в заданном параметре AccessToken.</span><span class="sxs-lookup"><span data-stu-id="ff93f-153">Account Id for access token in AccessToken parameter set.</span></span> <span data-ttu-id="ff93f-154">Идентификатор учетной записи для управляемой службы в установленном параметре ManagedService.</span><span class="sxs-lookup"><span data-stu-id="ff93f-154">Account Id for managed service in ManagedService parameter set.</span></span> <span data-ttu-id="ff93f-155">Может быть идентификатором управляемого ресурса службы или идентификатором связанного клиента. Чтобы использовать удостоверение SystemAssigned, оставьте это поле пустым.</span><span class="sxs-lookup"><span data-stu-id="ff93f-155">Can be a managed service resource Id, or the associated client id. To use the SystemAssigned identity, leave this field blank.</span></span>

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

### <span data-ttu-id="ff93f-156">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="ff93f-156">-ApplicationId</span></span>
<span data-ttu-id="ff93f-157">УЧАСТНИКОВ</span><span class="sxs-lookup"><span data-stu-id="ff93f-157">SPN</span></span>

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

### <span data-ttu-id="ff93f-158">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="ff93f-158">-CertificateThumbprint</span></span>
<span data-ttu-id="ff93f-159">Хэш сертификата (отпечаток)</span><span class="sxs-lookup"><span data-stu-id="ff93f-159">Certificate Hash (Thumbprint)</span></span>

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

### <span data-ttu-id="ff93f-160">-ContextName</span><span class="sxs-lookup"><span data-stu-id="ff93f-160">-ContextName</span></span>
<span data-ttu-id="ff93f-161">Имя контекста по умолчанию из этого имени входа.</span><span class="sxs-lookup"><span data-stu-id="ff93f-161">Name of the default context from this login.</span></span>  <span data-ttu-id="ff93f-162">Вы сможете выбрать этот контекст по этому имени после входа.</span><span class="sxs-lookup"><span data-stu-id="ff93f-162">You will be able to select this context by this name after login.</span></span>

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

### <span data-ttu-id="ff93f-163">-Credential</span><span class="sxs-lookup"><span data-stu-id="ff93f-163">-Credential</span></span>
<span data-ttu-id="ff93f-164">Указывает объект PSCredential.</span><span class="sxs-lookup"><span data-stu-id="ff93f-164">Specifies a PSCredential object.</span></span>
<span data-ttu-id="ff93f-165">Для получения дополнительных сведений о объекте PSCredential введите Get-Help Get-credentials.</span><span class="sxs-lookup"><span data-stu-id="ff93f-165">For more information about the PSCredential object, type Get-Help Get-Credential.</span></span>
<span data-ttu-id="ff93f-166">Объект PSCredential предоставляет идентификатор пользователя и пароль для учетных данных идентификатора организации, а также идентификатор приложения и секрет для учетных данных субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="ff93f-166">The PSCredential object provides the user ID and password for organizational ID credentials, or the application ID and secret for service principal credentials.</span></span>

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

### <span data-ttu-id="ff93f-167">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff93f-167">-DefaultProfile</span></span>
<span data-ttu-id="ff93f-168">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ff93f-168">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ff93f-169">-Environment</span><span class="sxs-lookup"><span data-stu-id="ff93f-169">-Environment</span></span>
<span data-ttu-id="ff93f-170">Среда, содержащая учетную запись, в которую нужно войти</span><span class="sxs-lookup"><span data-stu-id="ff93f-170">Environment containing the account to log into</span></span>

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

### <span data-ttu-id="ff93f-171">-Force</span><span class="sxs-lookup"><span data-stu-id="ff93f-171">-Force</span></span>
<span data-ttu-id="ff93f-172">Перезаписать существующий контекст с тем же именем, если таковое имеется.</span><span class="sxs-lookup"><span data-stu-id="ff93f-172">Overwrite the existing context with the same name, if any.</span></span>

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

### <span data-ttu-id="ff93f-173">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="ff93f-173">-GraphAccessToken</span></span>
<span data-ttu-id="ff93f-174">AccessToken для службы Graph</span><span class="sxs-lookup"><span data-stu-id="ff93f-174">AccessToken for Graph Service</span></span>

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

### <span data-ttu-id="ff93f-175">-Identity</span><span class="sxs-lookup"><span data-stu-id="ff93f-175">-Identity</span></span>
<span data-ttu-id="ff93f-176">Вход с учетной записью управляемой службы в текущем окружении.</span><span class="sxs-lookup"><span data-stu-id="ff93f-176">Login using managed service identity in the current environment.</span></span>

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

### <span data-ttu-id="ff93f-177">-KeyVaultAccessToken</span><span class="sxs-lookup"><span data-stu-id="ff93f-177">-KeyVaultAccessToken</span></span>
<span data-ttu-id="ff93f-178">Служба AccessToken для KeyVault</span><span class="sxs-lookup"><span data-stu-id="ff93f-178">AccessToken for KeyVault Service</span></span>

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

### <span data-ttu-id="ff93f-179">-ManagedServiceHostName</span><span class="sxs-lookup"><span data-stu-id="ff93f-179">-ManagedServiceHostName</span></span>
<span data-ttu-id="ff93f-180">Имя узла для логина управляемой службы</span><span class="sxs-lookup"><span data-stu-id="ff93f-180">Host name for managed service login</span></span>

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

### <span data-ttu-id="ff93f-181">-ManagedServicePort</span><span class="sxs-lookup"><span data-stu-id="ff93f-181">-ManagedServicePort</span></span>
<span data-ttu-id="ff93f-182">Номер порта для логина управляемой службы</span><span class="sxs-lookup"><span data-stu-id="ff93f-182">Port number for managed service login</span></span>

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

### <span data-ttu-id="ff93f-183">-ManagedServiceSecret</span><span class="sxs-lookup"><span data-stu-id="ff93f-183">-ManagedServiceSecret</span></span>
<span data-ttu-id="ff93f-184">Секрет, используемый для некоторых типов входных данных управляемой службы.</span><span class="sxs-lookup"><span data-stu-id="ff93f-184">Secret, used for some kinds of managed service login.</span></span>

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

### <span data-ttu-id="ff93f-185">-Scope</span><span class="sxs-lookup"><span data-stu-id="ff93f-185">-Scope</span></span>
<span data-ttu-id="ff93f-186">Определяет область изменений контекста, например, применяются ли изменения только к текущему процессу или ко всем сеансам, запускаемым этим пользователем.</span><span class="sxs-lookup"><span data-stu-id="ff93f-186">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="ff93f-187">-ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="ff93f-187">-ServicePrincipal</span></span>
<span data-ttu-id="ff93f-188">Указывает, что учетная запись проходит проверку подлинности путем предоставления учетных данных субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="ff93f-188">Indicates that this account authenticates by providing service principal credentials.</span></span>

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

### <span data-ttu-id="ff93f-189">-SkipContextPopulation</span><span class="sxs-lookup"><span data-stu-id="ff93f-189">-SkipContextPopulation</span></span>
<span data-ttu-id="ff93f-190">Пропускает заполнение контекста, если контексты не найдены.</span><span class="sxs-lookup"><span data-stu-id="ff93f-190">Skips context population if no contexts are found.</span></span>

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

### <span data-ttu-id="ff93f-191">-SkipValidation</span><span class="sxs-lookup"><span data-stu-id="ff93f-191">-SkipValidation</span></span>
<span data-ttu-id="ff93f-192">Пропуск проверки маркера доступа</span><span class="sxs-lookup"><span data-stu-id="ff93f-192">Skip validation for access token</span></span>

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

### <span data-ttu-id="ff93f-193">-Подписка</span><span class="sxs-lookup"><span data-stu-id="ff93f-193">-Subscription</span></span>
<span data-ttu-id="ff93f-194">Имя или идентификатор подписки</span><span class="sxs-lookup"><span data-stu-id="ff93f-194">Subscription Name or ID</span></span>

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

### <span data-ttu-id="ff93f-195">-Клиент</span><span class="sxs-lookup"><span data-stu-id="ff93f-195">-Tenant</span></span>
<span data-ttu-id="ff93f-196">Имя или идентификатор необязательного клиента</span><span class="sxs-lookup"><span data-stu-id="ff93f-196">Optional tenant name or ID</span></span>

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

### <span data-ttu-id="ff93f-197">-UseDeviceAuthentication</span><span class="sxs-lookup"><span data-stu-id="ff93f-197">-UseDeviceAuthentication</span></span>
<span data-ttu-id="ff93f-198">Использование проверки подлинности кода устройства вместо элемента управления браузером</span><span class="sxs-lookup"><span data-stu-id="ff93f-198">Use device code authentication instead of a browser control</span></span>

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

### <span data-ttu-id="ff93f-199">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ff93f-199">-Confirm</span></span>
<span data-ttu-id="ff93f-200">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ff93f-200">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff93f-201">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff93f-201">-WhatIf</span></span>
<span data-ttu-id="ff93f-202">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ff93f-202">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ff93f-203">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ff93f-203">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff93f-204">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff93f-204">CommonParameters</span></span>
<span data-ttu-id="ff93f-205">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ff93f-205">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff93f-206">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ff93f-206">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff93f-207">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ff93f-207">INPUTS</span></span>

### <span data-ttu-id="ff93f-208">System. String</span><span class="sxs-lookup"><span data-stu-id="ff93f-208">System.String</span></span>

## <span data-ttu-id="ff93f-209">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ff93f-209">OUTPUTS</span></span>

### <span data-ttu-id="ff93f-210">Microsoft. Azure. Commands. Profile. Models. Core. PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="ff93f-210">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile</span></span>

## <span data-ttu-id="ff93f-211">Пуск</span><span class="sxs-lookup"><span data-stu-id="ff93f-211">NOTES</span></span>

## <span data-ttu-id="ff93f-212">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ff93f-212">RELATED LINKS</span></span>
