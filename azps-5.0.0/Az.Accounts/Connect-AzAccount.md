---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/connect-azaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Connect-AzAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Connect-AzAccount.md
ms.openlocfilehash: 039ae434a28da0b8f320925c4e84c57571a74273
ms.sourcegitcommit: e30c11217b1ac93493fdd509fa71ac33510a98b5
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/29/2020
ms.locfileid: "94319463"
---
# <span data-ttu-id="8c0b9-101">Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="8c0b9-101">Connect-AzAccount</span></span>

## <span data-ttu-id="8c0b9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8c0b9-102">SYNOPSIS</span></span>
<span data-ttu-id="8c0b9-103">Подключитесь к Azure с учетной записью, прошедшей проверку подлинности, чтобы использовать командлеты из модулей PowerShell AZ.</span><span class="sxs-lookup"><span data-stu-id="8c0b9-103">Connect to Azure with an authenticated account for use with cmdlets from the Az PowerShell modules.</span></span>

## <span data-ttu-id="8c0b9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8c0b9-104">SYNTAX</span></span>

### <span data-ttu-id="8c0b9-105">UserWithSubscriptionId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8c0b9-105">UserWithSubscriptionId (Default)</span></span>
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] [-Subscription <String>] [-ContextName <String>]
 [-SkipContextPopulation] [-MaxContextPopulation <Int32>] [-UseDeviceAuthentication] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8c0b9-106">ServicePrincipalWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8c0b9-106">ServicePrincipalWithSubscriptionId</span></span>
```
Connect-AzAccount [-Environment <String>] -Credential <PSCredential> [-ServicePrincipal] -Tenant <String>
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-MaxContextPopulation <Int32>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8c0b9-107">UserWithCredential</span><span class="sxs-lookup"><span data-stu-id="8c0b9-107">UserWithCredential</span></span>
```
Connect-AzAccount [-Environment <String>] -Credential <PSCredential> [-Tenant <String>]
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-MaxContextPopulation <Int32>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8c0b9-108">ServicePrincipalCertificateWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8c0b9-108">ServicePrincipalCertificateWithSubscriptionId</span></span>
```
Connect-AzAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -Tenant <String> [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation]
 [-MaxContextPopulation <Int32>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c0b9-109">AccessTokenWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8c0b9-109">AccessTokenWithSubscriptionId</span></span>
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] -AccessToken <String> [-GraphAccessToken <String>]
 [-KeyVaultAccessToken <String>] -AccountId <String> [-Subscription <String>] [-ContextName <String>]
 [-SkipValidation] [-SkipContextPopulation] [-MaxContextPopulation <Int32>] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8c0b9-110">ManagedServiceLogin</span><span class="sxs-lookup"><span data-stu-id="8c0b9-110">ManagedServiceLogin</span></span>
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] [-AccountId <String>] [-Identity]
 [-ManagedServicePort <Int32>] [-ManagedServiceHostName <String>] [-ManagedServiceSecret <SecureString>]
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-MaxContextPopulation <Int32>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8c0b9-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8c0b9-111">DESCRIPTION</span></span>

<span data-ttu-id="8c0b9-112">`Connect-AzAccount`Командлет подключается к Azure с помощью учетной записи, прошедшей проверку подлинности, для использования с командлетами в модулях для AZ.</span><span class="sxs-lookup"><span data-stu-id="8c0b9-112">The `Connect-AzAccount` cmdlet connects to Azure with an authenticated account for use with cmdlets from the Az PowerShell modules.</span></span> <span data-ttu-id="8c0b9-113">Вы можете использовать эту учетную запись с проверкой подлинности только в запросах Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="8c0b9-113">You can use this authenticated account only with Azure Resource Manager requests.</span></span> <span data-ttu-id="8c0b9-114">Чтобы добавить учетную запись, прошедший проверку подлинности, с помощью средства управления службами, используйте `Add-AzureAccount` командлет из модуля Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8c0b9-114">To add an authenticated account for use with Service Management, use the `Add-AzureAccount` cmdlet from the Azure PowerShell module.</span></span> <span data-ttu-id="8c0b9-115">Если для текущего пользователя контекст не найден, список контекстов пользователя заполняется контекстом для каждой из первых 25 подписок.</span><span class="sxs-lookup"><span data-stu-id="8c0b9-115">If no context is found for the current user, the user's context list is populated with a context for each of their first 25 subscriptions.</span></span>
<span data-ttu-id="8c0b9-116">Список контекстов, созданных для пользователя, можно найти, выполнив `Get-AzContext -ListAvailable` .</span><span class="sxs-lookup"><span data-stu-id="8c0b9-116">The list of contexts created for the user can be found by running `Get-AzContext -ListAvailable`.</span></span> <span data-ttu-id="8c0b9-117">Чтобы пропустить это заполнение, укажите параметр ключа **SkipContextPopulation** .</span><span class="sxs-lookup"><span data-stu-id="8c0b9-117">To skip this context population, specify the **SkipContextPopulation** switch parameter.</span></span> <span data-ttu-id="8c0b9-118">После выполнения этого командлета вы можете отключиться от учетной записи Azure с помощью `Disconnect-AzAccount` .</span><span class="sxs-lookup"><span data-stu-id="8c0b9-118">After executing this cmdlet, you can disconnect from an Azure account using `Disconnect-AzAccount`.</span></span>

## <span data-ttu-id="8c0b9-119">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8c0b9-119">EXAMPLES</span></span>

### <span data-ttu-id="8c0b9-120">Пример 1: подключение к учетной записи Azure</span><span class="sxs-lookup"><span data-stu-id="8c0b9-120">Example 1: Connect to an Azure account</span></span>

<span data-ttu-id="8c0b9-121">В этом примере выполняется подключение к учетной записи Azure.</span><span class="sxs-lookup"><span data-stu-id="8c0b9-121">This example connects to an Azure account.</span></span> <span data-ttu-id="8c0b9-122">Укажите учетную запись Майкрософт или идентификационный номер Организации.</span><span class="sxs-lookup"><span data-stu-id="8c0b9-122">You must provide a Microsoft account or organizational ID credentials.</span></span> <span data-ttu-id="8c0b9-123">Если для ваших учетных данных включена многофакторная проверка подлинности, вы должны войти в систему с помощью интерактивного режима или воспользоваться проверкой подлинности субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="8c0b9-123">If multi-factor authentication is enabled for your credentials, you must log in using the interactive option or use service principal authentication.</span></span>

```powershell
Connect-AzAccount
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="8c0b9-124">Пример 2: (только для Windows PowerShell 5,1) подключение к Azure с использованием учетных данных идентификатора Организации</span><span class="sxs-lookup"><span data-stu-id="8c0b9-124">Example 2: (Windows PowerShell 5.1 only) Connect to Azure using organizational ID credentials</span></span>

<span data-ttu-id="8c0b9-125">Этот сценарий работает только в Windows PowerShell 5,1.</span><span class="sxs-lookup"><span data-stu-id="8c0b9-125">This scenario works only in Windows PowerShell 5.1.</span></span> <span data-ttu-id="8c0b9-126">Первая команда запрашивает учетные данные пользователя и сохраняет их в `$Credential` переменной.</span><span class="sxs-lookup"><span data-stu-id="8c0b9-126">The first command prompts for user credentials and stores them in the `$Credential` variable.</span></span> <span data-ttu-id="8c0b9-127">Вторая команда подключается к учетной записи Azure с использованием учетных данных, хранящихся в `$Credential` .</span><span class="sxs-lookup"><span data-stu-id="8c0b9-127">The second command connects to an Azure account using the credentials stored in `$Credential`.</span></span> <span data-ttu-id="8c0b9-128">Эта учетная запись проходит проверку подлинности с помощью Azure с использованием учетных данных идентификатора организации.</span><span class="sxs-lookup"><span data-stu-id="8c0b9-128">This account authenticates with Azure using organizational ID credentials.</span></span>

```powershell
$Credential = Get-Credential
Connect-AzAccount -Credential $Credential
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="8c0b9-129">Пример 3: подключение к Azure с использованием учетной записи субъекта-службы</span><span class="sxs-lookup"><span data-stu-id="8c0b9-129">Example 3: Connect to Azure using a service principal account</span></span>

<span data-ttu-id="8c0b9-130">Первая команда запрашивает учетные данные субъекта-службы и сохраняет их в `$Credential` переменной.</span><span class="sxs-lookup"><span data-stu-id="8c0b9-130">The first command prompts for service principal credentials and stores them in the `$Credential` variable.</span></span> <span data-ttu-id="8c0b9-131">Введите идентификатор приложения для имени пользователя и секрета участника-службы в качестве пароля при появлении соответствующего запроса.</span><span class="sxs-lookup"><span data-stu-id="8c0b9-131">Enter your application ID for the username and service principal secret as the password when prompted.</span></span> <span data-ttu-id="8c0b9-132">Вторая команда подключает указанного клиента Azure с использованием учетных данных субъекта-службы, хранящихся в `$Credential` переменной.</span><span class="sxs-lookup"><span data-stu-id="8c0b9-132">The second command connects the specified Azure tenant using the service principal credentials stored in the `$Credential` variable.</span></span> <span data-ttu-id="8c0b9-133">Параметр ключа **ServicePrincipal** указывает, что учетная запись проходит проверку подлинности субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="8c0b9-133">The **ServicePrincipal** switch parameter indicates that the account authenticates as a service principal.</span></span>

```powershell
$Credential = Get-Credential
Connect-AzAccount -Credential $Credential -Tenant 'xxxx-xxxx-xxxx-xxxx' -ServicePrincipal
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
xxxx-xxxx-xxxx-xxxx    Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="8c0b9-134">Пример 4: использование интерактивного входа для подключения к определенному клиенту и подписке</span><span class="sxs-lookup"><span data-stu-id="8c0b9-134">Example 4: Use an interactive login to connect to a specific tenant and subscription</span></span>

<span data-ttu-id="8c0b9-135">В этом примере подключение к учетной записи Azure осуществляется с помощью указанного клиента и подписки.</span><span class="sxs-lookup"><span data-stu-id="8c0b9-135">This example connects to an Azure account with the specified tenant and subscription.</span></span>

```powershell
Connect-AzAccount -Tenant 'xxxx-xxxx-xxxx-xxxx' -SubscriptionId 'yyyy-yyyy-yyyy-yyyy'
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="8c0b9-136">Пример 5: подключение с использованием управляемого удостоверения службы</span><span class="sxs-lookup"><span data-stu-id="8c0b9-136">Example 5: Connect using a Managed Service Identity</span></span>

<span data-ttu-id="8c0b9-137">В этом примере выполняется соединение с помощью идентификатора управляемой службы (MSI) среды узла.</span><span class="sxs-lookup"><span data-stu-id="8c0b9-137">This example connects using the Managed Service Identity (MSI) of the host environment.</span></span> <span data-ttu-id="8c0b9-138">Например, вы входите в Azure с виртуальной машины, назначенной MSI.</span><span class="sxs-lookup"><span data-stu-id="8c0b9-138">For example, you sign into Azure from a virtual machine that has an assigned MSI.</span></span>

```powershell
Connect-AzAccount -Identity
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
MSI@50342              Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="8c0b9-139">Пример 6: подключение с помощью учетной записи удостоверения управляемой службы и ClientId</span><span class="sxs-lookup"><span data-stu-id="8c0b9-139">Example 6: Connect using Managed Service Identity login and ClientId</span></span>

<span data-ttu-id="8c0b9-140">В этом примере выполняется соединение с использованием управляемого удостоверения службы **myUserAssignedIdentity**.</span><span class="sxs-lookup"><span data-stu-id="8c0b9-140">This example connects using the Managed Service Identity of **myUserAssignedIdentity**.</span></span> <span data-ttu-id="8c0b9-141">Он добавляет удостоверение пользователя к виртуальной машине, а затем подключает его с помощью ClientId идентификатора, назначенного пользователю.</span><span class="sxs-lookup"><span data-stu-id="8c0b9-141">It adds the user assigned identity to the virtual machine, then connects using the ClientId of the user assigned identity.</span></span> <span data-ttu-id="8c0b9-142">Дополнительные сведения можно найти [в разделе Настройка управляемых идентификаторов для ресурсов Azure на виртуальной машине Azure](/azure/active-directory/managed-identities-azure-resources/qs-configure-powershell-windows-vm).</span><span class="sxs-lookup"><span data-stu-id="8c0b9-142">For more information, see [Configure managed identities for Azure resources on an Azure VM](/azure/active-directory/managed-identities-azure-resources/qs-configure-powershell-windows-vm).</span></span>

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

### <span data-ttu-id="8c0b9-143">Пример 7: подключение с помощью сертификатов</span><span class="sxs-lookup"><span data-stu-id="8c0b9-143">Example 7: Connect using certificates</span></span>

<span data-ttu-id="8c0b9-144">В этом примере подключение к учетной записи Azure осуществляется с помощью проверки подлинности субъекта-службы на основе сертификата.</span><span class="sxs-lookup"><span data-stu-id="8c0b9-144">This example connects to an Azure account using certificate-based service principal authentication.</span></span>
<span data-ttu-id="8c0b9-145">Субъект-служба, используемая для проверки подлинности, должна быть создана с помощью указанного сертификата.</span><span class="sxs-lookup"><span data-stu-id="8c0b9-145">The service principal used for authentication must be created with the specified certificate.</span></span> <span data-ttu-id="8c0b9-146">Дополнительные сведения о создании самозаверяющих сертификатов и назначении им разрешений можно найти [в разделе Использование Azure PowerShell для создания субъекта-службы с сертификатом](/azure/active-directory/develop/howto-authenticate-service-principal-powershell)</span><span class="sxs-lookup"><span data-stu-id="8c0b9-146">For more information on creating a self-signed certificates and assigning them permissions, see [Use Azure PowerShell to create a service principal with a certificate](/azure/active-directory/develop/howto-authenticate-service-principal-powershell)</span></span>

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

## <span data-ttu-id="8c0b9-147">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8c0b9-147">PARAMETERS</span></span>

### <span data-ttu-id="8c0b9-148">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="8c0b9-148">-AccessToken</span></span>

<span data-ttu-id="8c0b9-149">Задает маркер доступа.</span><span class="sxs-lookup"><span data-stu-id="8c0b9-149">Specifies an access token.</span></span>

> [!CAUTION]
> <span data-ttu-id="8c0b9-150">Маркеры доступа — это тип учетных данных.</span><span class="sxs-lookup"><span data-stu-id="8c0b9-150">Access tokens are a type of credential.</span></span> <span data-ttu-id="8c0b9-151">Вы должны принять меры предосторожности для обеспечения конфиденциальности.</span><span class="sxs-lookup"><span data-stu-id="8c0b9-151">You should take the appropriate security precautions to keep them confidential.</span></span> <span data-ttu-id="8c0b9-152">Маркеры доступа также допускают тайм-аут и могут препятствовать завершению выполнения длительных задач.</span><span class="sxs-lookup"><span data-stu-id="8c0b9-152">Access tokens also timeout and may prevent long running tasks from completing.</span></span>

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

### <span data-ttu-id="8c0b9-153">-AccountId</span><span class="sxs-lookup"><span data-stu-id="8c0b9-153">-AccountId</span></span>

<span data-ttu-id="8c0b9-154">Идентификатор учетной записи для маркера доступа в заданном параметре **AccessToken** .</span><span class="sxs-lookup"><span data-stu-id="8c0b9-154">Account ID for access token in **AccessToken** parameter set.</span></span> <span data-ttu-id="8c0b9-155">Идентификатор учетной записи для управляемой службы в установленном параметре **ManagedService** .</span><span class="sxs-lookup"><span data-stu-id="8c0b9-155">Account ID for managed service in **ManagedService** parameter set.</span></span> <span data-ttu-id="8c0b9-156">Может быть ИДЕНТИФИКАТОРом управляемого ресурса службы или ИДЕНТИФИКАТОРом связанного клиента.</span><span class="sxs-lookup"><span data-stu-id="8c0b9-156">Can be a managed service resource ID, or the associated client ID.</span></span>
<span data-ttu-id="8c0b9-157">Чтобы использовать удостоверение, назначенное системой, оставьте это поле пустым.</span><span class="sxs-lookup"><span data-stu-id="8c0b9-157">To use the system assigned identity, leave this field blank.</span></span>

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

### <span data-ttu-id="8c0b9-158">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="8c0b9-158">-ApplicationId</span></span>

<span data-ttu-id="8c0b9-159">Идентификатор приложения субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="8c0b9-159">Application ID of the service principal.</span></span>

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

### <span data-ttu-id="8c0b9-160">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="8c0b9-160">-CertificateThumbprint</span></span>

<span data-ttu-id="8c0b9-161">Хэш или отпечаток сертификата.</span><span class="sxs-lookup"><span data-stu-id="8c0b9-161">Certificate Hash or Thumbprint.</span></span>

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

### <span data-ttu-id="8c0b9-162">-ContextName</span><span class="sxs-lookup"><span data-stu-id="8c0b9-162">-ContextName</span></span>

<span data-ttu-id="8c0b9-163">Имя контекста Azure по умолчанию для этого имени входа.</span><span class="sxs-lookup"><span data-stu-id="8c0b9-163">Name of the default Azure context for this login.</span></span> <span data-ttu-id="8c0b9-164">Дополнительные сведения о контекстах Azure см. в разделе [контекстные объекты Azure PowerShell](/powershell/azure/context-persistence).</span><span class="sxs-lookup"><span data-stu-id="8c0b9-164">For more information about Azure contexts, see [Azure PowerShell context objects](/powershell/azure/context-persistence).</span></span>

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

### <span data-ttu-id="8c0b9-165">-Credential</span><span class="sxs-lookup"><span data-stu-id="8c0b9-165">-Credential</span></span>

<span data-ttu-id="8c0b9-166">Указывает объект **PSCredential** .</span><span class="sxs-lookup"><span data-stu-id="8c0b9-166">Specifies a **PSCredential** object.</span></span> <span data-ttu-id="8c0b9-167">Чтобы получить дополнительные сведения о объекте **PSCredential** , введите `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="8c0b9-167">For more information about the **PSCredential** object, type `Get-Help Get-Credential`.</span></span> <span data-ttu-id="8c0b9-168">Объект **PSCredential** предоставляет идентификатор пользователя и пароль для учетных данных идентификатора организации, а также идентификатор приложения и секрет для учетных данных субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="8c0b9-168">The **PSCredential** object provides the user ID and password for organizational ID credentials, or the application ID and secret for service principal credentials.</span></span>

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

### <span data-ttu-id="8c0b9-169">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c0b9-169">-DefaultProfile</span></span>

<span data-ttu-id="8c0b9-170">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8c0b9-170">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8c0b9-171">-Environment</span><span class="sxs-lookup"><span data-stu-id="8c0b9-171">-Environment</span></span>

<span data-ttu-id="8c0b9-172">Среда с учетной записью Azure.</span><span class="sxs-lookup"><span data-stu-id="8c0b9-172">Environment containing the Azure account.</span></span>

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

### <span data-ttu-id="8c0b9-173">-Force</span><span class="sxs-lookup"><span data-stu-id="8c0b9-173">-Force</span></span>

<span data-ttu-id="8c0b9-174">Перезаписать существующий контекст с тем же именем без запроса.</span><span class="sxs-lookup"><span data-stu-id="8c0b9-174">Overwrite the existing context with the same name without prompting.</span></span>

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

### <span data-ttu-id="8c0b9-175">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="8c0b9-175">-GraphAccessToken</span></span>

<span data-ttu-id="8c0b9-176">AccessToken для службы Graph.</span><span class="sxs-lookup"><span data-stu-id="8c0b9-176">AccessToken for Graph Service.</span></span>

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

### <span data-ttu-id="8c0b9-177">-Identity</span><span class="sxs-lookup"><span data-stu-id="8c0b9-177">-Identity</span></span>

<span data-ttu-id="8c0b9-178">Вход с учетной записью управляемой службы.</span><span class="sxs-lookup"><span data-stu-id="8c0b9-178">Login using a Managed Service Identity.</span></span>

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

### <span data-ttu-id="8c0b9-179">-KeyVaultAccessToken</span><span class="sxs-lookup"><span data-stu-id="8c0b9-179">-KeyVaultAccessToken</span></span>

<span data-ttu-id="8c0b9-180">AccessToken для KeyVault услуги.</span><span class="sxs-lookup"><span data-stu-id="8c0b9-180">AccessToken for KeyVault Service.</span></span>

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

### <span data-ttu-id="8c0b9-181">-ManagedServiceHostName</span><span class="sxs-lookup"><span data-stu-id="8c0b9-181">-ManagedServiceHostName</span></span>

<span data-ttu-id="8c0b9-182">Имя узла для управляемой службы.</span><span class="sxs-lookup"><span data-stu-id="8c0b9-182">Host name for the managed service.</span></span>

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

### <span data-ttu-id="8c0b9-183">-ManagedServicePort</span><span class="sxs-lookup"><span data-stu-id="8c0b9-183">-ManagedServicePort</span></span>

<span data-ttu-id="8c0b9-184">Номер порта управляемой службы.</span><span class="sxs-lookup"><span data-stu-id="8c0b9-184">Port number for the managed service.</span></span>

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

### <span data-ttu-id="8c0b9-185">-ManagedServiceSecret</span><span class="sxs-lookup"><span data-stu-id="8c0b9-185">-ManagedServiceSecret</span></span>

<span data-ttu-id="8c0b9-186">Маркер для логина управляемой службы.</span><span class="sxs-lookup"><span data-stu-id="8c0b9-186">Token for the managed service login.</span></span>

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

### <span data-ttu-id="8c0b9-187">-MaxContextPopulation</span><span class="sxs-lookup"><span data-stu-id="8c0b9-187">-MaxContextPopulation</span></span>

<span data-ttu-id="8c0b9-188">Максимальный номер подписки для заполнения контекстов после входа.</span><span class="sxs-lookup"><span data-stu-id="8c0b9-188">Max subscription number to populate contexts after login.</span></span> <span data-ttu-id="8c0b9-189">По умолчанию — 25.</span><span class="sxs-lookup"><span data-stu-id="8c0b9-189">Default is 25.</span></span> <span data-ttu-id="8c0b9-190">Для заполнения всех подписок на контексты установите значение-1.</span><span class="sxs-lookup"><span data-stu-id="8c0b9-190">To populate all subscriptions to contexts, set to -1.</span></span>

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

### <span data-ttu-id="8c0b9-191">-Scope</span><span class="sxs-lookup"><span data-stu-id="8c0b9-191">-Scope</span></span>

<span data-ttu-id="8c0b9-192">Определяет область изменений контекста, например, применяются ли изменения только к текущему процессу или ко всем сеансам, запускаемым этим пользователем.</span><span class="sxs-lookup"><span data-stu-id="8c0b9-192">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="8c0b9-193">-ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="8c0b9-193">-ServicePrincipal</span></span>

<span data-ttu-id="8c0b9-194">Указывает, что учетная запись проходит проверку подлинности путем предоставления учетных данных субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="8c0b9-194">Indicates that this account authenticates by providing service principal credentials.</span></span>

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

### <span data-ttu-id="8c0b9-195">-SkipContextPopulation</span><span class="sxs-lookup"><span data-stu-id="8c0b9-195">-SkipContextPopulation</span></span>

<span data-ttu-id="8c0b9-196">Пропускает заполнение контекста, если контексты не найдены.</span><span class="sxs-lookup"><span data-stu-id="8c0b9-196">Skips context population if no contexts are found.</span></span>

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

### <span data-ttu-id="8c0b9-197">-SkipValidation</span><span class="sxs-lookup"><span data-stu-id="8c0b9-197">-SkipValidation</span></span>

<span data-ttu-id="8c0b9-198">Пропуск проверки маркера доступа.</span><span class="sxs-lookup"><span data-stu-id="8c0b9-198">Skip validation for access token.</span></span>

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

### <span data-ttu-id="8c0b9-199">-Подписка</span><span class="sxs-lookup"><span data-stu-id="8c0b9-199">-Subscription</span></span>

<span data-ttu-id="8c0b9-200">Имя или идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="8c0b9-200">Subscription Name or ID.</span></span>

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

### <span data-ttu-id="8c0b9-201">-Клиент</span><span class="sxs-lookup"><span data-stu-id="8c0b9-201">-Tenant</span></span>

<span data-ttu-id="8c0b9-202">Необязательное имя клиента или идентификатор.</span><span class="sxs-lookup"><span data-stu-id="8c0b9-202">Optional tenant name or ID.</span></span>

> [!NOTE]
> <span data-ttu-id="8c0b9-203">Из-за ограничений текущего API необходимо использовать идентификатор клиента вместо имени клиента при подключении к учетной записи "бизнес-бизнес" (B2B).</span><span class="sxs-lookup"><span data-stu-id="8c0b9-203">Due to limitations of the current API, you must use a tenant ID instead of a tenant name when connecting with a business-to-business (B2B) account.</span></span>

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

### <span data-ttu-id="8c0b9-204">-UseDeviceAuthentication</span><span class="sxs-lookup"><span data-stu-id="8c0b9-204">-UseDeviceAuthentication</span></span>

<span data-ttu-id="8c0b9-205">Используйте проверку подлинности кода устройства вместо элемента управления браузера.</span><span class="sxs-lookup"><span data-stu-id="8c0b9-205">Use device code authentication instead of a browser control.</span></span>

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

### <span data-ttu-id="8c0b9-206">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8c0b9-206">-Confirm</span></span>

<span data-ttu-id="8c0b9-207">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8c0b9-207">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c0b9-208">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c0b9-208">-WhatIf</span></span>

<span data-ttu-id="8c0b9-209">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8c0b9-209">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8c0b9-210">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8c0b9-210">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c0b9-211">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c0b9-211">CommonParameters</span></span>
<span data-ttu-id="8c0b9-212">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8c0b9-212">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c0b9-213">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8c0b9-213">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c0b9-214">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8c0b9-214">INPUTS</span></span>

### <span data-ttu-id="8c0b9-215">System. String</span><span class="sxs-lookup"><span data-stu-id="8c0b9-215">System.String</span></span>

## <span data-ttu-id="8c0b9-216">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8c0b9-216">OUTPUTS</span></span>

### <span data-ttu-id="8c0b9-217">Microsoft. Azure. Commands. Profile. Models. Core. PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="8c0b9-217">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile</span></span>

## <span data-ttu-id="8c0b9-218">Пуск</span><span class="sxs-lookup"><span data-stu-id="8c0b9-218">NOTES</span></span>

## <span data-ttu-id="8c0b9-219">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8c0b9-219">RELATED LINKS</span></span>
