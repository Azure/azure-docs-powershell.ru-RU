---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/add-azurermaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Connect-AzureRmAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Connect-AzureRmAccount.md
ms.openlocfilehash: 01cc9210e57edbb19caa8406e9015b36942b99d4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557268"
---
# <span data-ttu-id="329fe-101">Connect-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="329fe-101">Connect-AzureRmAccount</span></span>

## <span data-ttu-id="329fe-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="329fe-102">SYNOPSIS</span></span>
<span data-ttu-id="329fe-103">Подключитесь к Azure с учетной записью, прошедшим проверку подлинности, для использования с запросом командлетов Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="329fe-103">Connect to Azure with an authenticated account for use with Azure Resource Manager cmdlet requests.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="329fe-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="329fe-104">SYNTAX</span></span>

### <span data-ttu-id="329fe-105">UserWithSubscriptionId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="329fe-105">UserWithSubscriptionId (Default)</span></span>
```
Connect-AzureRmAccount [-Environment <String>] [[-Credential] <PSCredential>] [-TenantId <String>]
 [-Subscription <String>] [-ContextName <String>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="329fe-106">ServicePrincipalWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="329fe-106">ServicePrincipalWithSubscriptionId</span></span>
```
Connect-AzureRmAccount [-Environment <String>] [-Credential] <PSCredential> [-ServicePrincipal]
 -TenantId <String> [-Subscription <String>] [-ContextName <String>] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="329fe-107">ServicePrincipalCertificateWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="329fe-107">ServicePrincipalCertificateWithSubscriptionId</span></span>
```
Connect-AzureRmAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -TenantId <String> [-Subscription <String>] [-ContextName <String>] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="329fe-108">AccessTokenWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="329fe-108">AccessTokenWithSubscriptionId</span></span>
```
Connect-AzureRmAccount [-Environment <String>] [-TenantId <String>] -AccessToken <String>
 [-GraphAccessToken <String>] [-KeyVaultAccessToken <String>] -AccountId <String> [-Subscription <String>]
 [-ContextName <String>] [-SkipValidation] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="329fe-109">ManagedServiceLogin</span><span class="sxs-lookup"><span data-stu-id="329fe-109">ManagedServiceLogin</span></span>
```
Connect-AzureRmAccount [-Environment <String>] [-TenantId <String>] [-AccountId <String>] [-Identity]
 [-ManagedServicePort <Int32>] [-ManagedServiceHostName <String>] [-Subscription <String>]
 [-ContextName <String>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="329fe-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="329fe-110">DESCRIPTION</span></span>
<span data-ttu-id="329fe-111">Командлет Connect-AzureRmAccount подключает к Azure учетную запись с проверкой подлинности для использования с запросом командлета диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="329fe-111">The Connect-AzureRmAccount cmdlet connects to Azure with an authenticated account for use with Azure Resource Manager cmdlet requests.</span></span>

<span data-ttu-id="329fe-112">Вы можете использовать эту учетную запись с проверкой подлинности только для командлетов Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="329fe-112">You can use this authenticated account only with Azure Resource Manager cmdlets.</span></span>

<span data-ttu-id="329fe-113">Чтобы добавить учетную запись, прошедший проверку подлинности, с помощью командлетов управления службами, используйте Add-AzureAccount или Import-AzurePublishSettingsFile.</span><span class="sxs-lookup"><span data-stu-id="329fe-113">To add an authenticated account for use with Service Management cmdlets, use the Add-AzureAccount or the Import-AzurePublishSettingsFile cmdlet.</span></span>

<span data-ttu-id="329fe-114">После выполнения этого командлета вы можете отключиться от учетной записи Azure с помощью команды Disconnect-AzureRmAccount.</span><span class="sxs-lookup"><span data-stu-id="329fe-114">After executing this cmdlet, you can disconnect from an Azure account using Disconnect-AzureRmAccount.</span></span>

## <span data-ttu-id="329fe-115">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="329fe-115">EXAMPLES</span></span>

### <span data-ttu-id="329fe-116">Пример 1: использование интерактивного входа для подключения к учетной записи Azure</span><span class="sxs-lookup"><span data-stu-id="329fe-116">Example 1: Use an interactive login to connect to an Azure account</span></span>
```
PS C:\> Connect-AzureRmAccount
Account: azureuser@contoso.com
Environment: AzureCloud
Subscription: xxxx-xxxx-xxxx-xxxx
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="329fe-117">Эта команда соединяется с учетной записью Azure.</span><span class="sxs-lookup"><span data-stu-id="329fe-117">This command connects to an Azure account.</span></span>

<span data-ttu-id="329fe-118">Чтобы запустить командлеты диспетчера ресурсов Azure с этой учетной записью, необходимо задать учетные данные учетной записи Майкрософт или идентификатора организации в запросе.</span><span class="sxs-lookup"><span data-stu-id="329fe-118">To run Azure Resource Manager cmdlets with this account, you must provide Microsoft account or organizational ID credentials at the prompt.</span></span>

<span data-ttu-id="329fe-119">Если для ваших учетных данных включена многофакторная проверка подлинности, вы должны войти в систему с помощью интерактивного режима или воспользоваться проверкой подлинности субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="329fe-119">If multi-factor authentication is enabled for your credentials, you must log in using the interactive option or use service principal authentication.</span></span>

### <span data-ttu-id="329fe-120">Пример 2: подключение к учетной записи Azure с использованием учетных данных идентификатора Организации</span><span class="sxs-lookup"><span data-stu-id="329fe-120">Example 2: Connect to an Azure account using organizational ID credentials</span></span>
```
PS C:\> $Credential = Get-Credential
PS C:\> Connect-AzureRmAccount -Credential $Credential
Account: azureuser@contoso.com
Environment: AzureChinaCloud
Subscription: xxxx-xxxx-xxxx-xxxx
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="329fe-121">Первая команда получает учетные данные пользователя, а затем сохраняет их в переменной $Credential.</span><span class="sxs-lookup"><span data-stu-id="329fe-121">The first command gets the user credentials, and then stores them in the $Credential variable.</span></span>

<span data-ttu-id="329fe-122">Вторая команда подключается к учетной записи Azure с использованием учетных данных, которые хранятся в $Credential.</span><span class="sxs-lookup"><span data-stu-id="329fe-122">The second command connects to an Azure account using the credentials stored in $Credential.</span></span>

<span data-ttu-id="329fe-123">Эта учетная запись проходит проверку подлинности с помощью диспетчера ресурсов Azure с использованием учетных данных идентификатора организации.</span><span class="sxs-lookup"><span data-stu-id="329fe-123">This account authenticates with Azure Resource Manager using organizational ID credentials.</span></span>

<span data-ttu-id="329fe-124">Для запуска командлетов диспетчера ресурсов Azure с этой учетной записью нельзя использовать многофакторную проверку подлинности или учетные данные учетной записи Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="329fe-124">You cannot use multi-factor authentication or Microsoft account credentials to run Azure Resource Manager cmdlets with this account.</span></span>

### <span data-ttu-id="329fe-125">Пример 3: подключение к учетной записи субъекта-службы Azure</span><span class="sxs-lookup"><span data-stu-id="329fe-125">Example 3: Connect to an Azure service principal account</span></span>
```
PS C:\> $Credential = Get-Credential
PS C:\> Connect-AzureRmAccount -Credential $Credential -Tenant "xxxx-xxxx-xxxx-xxxx" -ServicePrincipal
Account: xxxx-xxxx-xxxx-xxxx
Environment: AzureCloud
Subscription: yyyy-yyyy-yyyy-yyyy
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="329fe-126">Первая команда получает учетные данные пользователя, а затем сохраняет их в переменной $Credential.</span><span class="sxs-lookup"><span data-stu-id="329fe-126">The first command gets the user credentials, and then stores them in the $Credential variable.</span></span>

<span data-ttu-id="329fe-127">Вторая команда подключается к Azure с использованием учетных данных субъекта-службы, хранящихся в $Credential для указанного клиента.</span><span class="sxs-lookup"><span data-stu-id="329fe-127">The second command connect to Azure using the service principal credentials stored in $Credential for the specified Tenant.</span></span>

<span data-ttu-id="329fe-128">Параметр ключа ServicePrincipal указывает, что учетная запись проходит проверку подлинности субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="329fe-128">The ServicePrincipal switch parameter indicates that the account authenticates as a service principal.</span></span>

### <span data-ttu-id="329fe-129">Пример 4: использование интерактивного входа для подключения к учетной записи для определенного клиента и подписки</span><span class="sxs-lookup"><span data-stu-id="329fe-129">Example 4: Use an interactive login to connect to an account for a specific tenant and subscription</span></span>
```
PS C:\> Connect-AzureRmAccount -Tenant "xxxx-xxxx-xxxx-xxxx" -SubscriptionId "yyyy-yyyy-yyyy-yyyy"
Account: pfuller@contoso.com
Environment: AzureCloud
Subscription: yyyy-yyyy-yyyy-yyyy
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="329fe-130">Эта команда соединяется с учетной записью Azure и настроила AzureRM PowerShell для запуска командлетов для указанного клиента и подписки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="329fe-130">This command connects to an Azure account and configured AzureRM PowerShell to run cmdlets for the specified tenant and subscription by default.</span></span>

### <span data-ttu-id="329fe-131">Пример 5: Добавление учетной записи с помощью имени входа для удостоверения управляемой службы</span><span class="sxs-lookup"><span data-stu-id="329fe-131">Example 5: Add an Account Using Managed Service Identity Login</span></span>
```
PS C:\>Add-AzureRmAccount -MSI
Account: MSI@50342
Environment: AzureCloud
Subscription: yyyy-yyyy-yyyy-yyyy
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="329fe-132">Эта команда выполняет вход в учетную запись управляемой службы среды узла (например, если она выполняется в VirtualMachine с назначенным идентификатором управляемой службы, это позволит коду войти в систему с использованием этого назначенного удостоверения).</span><span class="sxs-lookup"><span data-stu-id="329fe-132">This command logs in using the managed service identity of the host environment (for example, if executed on a VirtualMachine with an assigned Managed Service Identity, this will allow the code to login using that assigned identity)</span></span>

## <span data-ttu-id="329fe-133">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="329fe-133">PARAMETERS</span></span>

### <span data-ttu-id="329fe-134">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="329fe-134">-AccessToken</span></span>
<span data-ttu-id="329fe-135">Задает маркер доступа.</span><span class="sxs-lookup"><span data-stu-id="329fe-135">Specifies an access token.</span></span>

```yaml
Type: String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="329fe-136">-AccountId</span><span class="sxs-lookup"><span data-stu-id="329fe-136">-AccountId</span></span>
<span data-ttu-id="329fe-137">Идентификатор учетной записи для маркера доступа</span><span class="sxs-lookup"><span data-stu-id="329fe-137">Account Id for access token</span></span>

```yaml
Type: String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ManagedServiceLogin
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="329fe-138">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="329fe-138">-ApplicationId</span></span>
<span data-ttu-id="329fe-139">УЧАСТНИКОВ</span><span class="sxs-lookup"><span data-stu-id="329fe-139">SPN</span></span>

```yaml
Type: String
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="329fe-140">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="329fe-140">-CertificateThumbprint</span></span>
<span data-ttu-id="329fe-141">Хэш сертификата (отпечаток)</span><span class="sxs-lookup"><span data-stu-id="329fe-141">Certificate Hash (Thumbprint)</span></span>

```yaml
Type: String
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="329fe-142">-ContextName</span><span class="sxs-lookup"><span data-stu-id="329fe-142">-ContextName</span></span>
<span data-ttu-id="329fe-143">Имя контекста по умолчанию из этого имени входа.</span><span class="sxs-lookup"><span data-stu-id="329fe-143">Name of the default context from this login.</span></span>  <span data-ttu-id="329fe-144">Вы сможете выбрать этот контекст по этому имени после входа.</span><span class="sxs-lookup"><span data-stu-id="329fe-144">You will be able to select this context by this name after login.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="329fe-145">-Credential</span><span class="sxs-lookup"><span data-stu-id="329fe-145">-Credential</span></span>
<span data-ttu-id="329fe-146">Указывает объект PSCredential.</span><span class="sxs-lookup"><span data-stu-id="329fe-146">Specifies a PSCredential object.</span></span>
<span data-ttu-id="329fe-147">Для получения дополнительных сведений о объекте PSCredential введите Get-Help Get-credentials.</span><span class="sxs-lookup"><span data-stu-id="329fe-147">For more information about the PSCredential object, type Get-Help Get-Credential.</span></span>

<span data-ttu-id="329fe-148">Объект PSCredential предоставляет идентификатор пользователя и пароль для учетных данных идентификатора организации, а также идентификатор приложения и секрет для учетных данных субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="329fe-148">The PSCredential object provides the user ID and password for organizational ID credentials, or the application ID and secret for service principal credentials.</span></span>

```yaml
Type: PSCredential
Parameter Sets: UserWithSubscriptionId
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: PSCredential
Parameter Sets: ServicePrincipalWithSubscriptionId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="329fe-149">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="329fe-149">-DefaultProfile</span></span>
<span data-ttu-id="329fe-150">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="329fe-150">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="329fe-151">-Environment</span><span class="sxs-lookup"><span data-stu-id="329fe-151">-Environment</span></span>
<span data-ttu-id="329fe-152">Среда, содержащая учетную запись, в которую нужно войти</span><span class="sxs-lookup"><span data-stu-id="329fe-152">Environment containing the account to log into</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: EnvironmentName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="329fe-153">-Force</span><span class="sxs-lookup"><span data-stu-id="329fe-153">-Force</span></span>
<span data-ttu-id="329fe-154">Перезаписать существующий контекст с тем же именем, если таковое имеется.</span><span class="sxs-lookup"><span data-stu-id="329fe-154">Overwrite the existing context with the same name, if any.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="329fe-155">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="329fe-155">-GraphAccessToken</span></span>
<span data-ttu-id="329fe-156">AccessToken для службы Graph</span><span class="sxs-lookup"><span data-stu-id="329fe-156">AccessToken for Graph Service</span></span>

```yaml
Type: String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="329fe-157">-Identity</span><span class="sxs-lookup"><span data-stu-id="329fe-157">-Identity</span></span>
<span data-ttu-id="329fe-158">Вход с учетной записью управляемой службы в текущем окружении.</span><span class="sxs-lookup"><span data-stu-id="329fe-158">Login using managed service identity in the current environment.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ManagedServiceLogin
Aliases: MSI, ManagedService

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="329fe-159">-KeyVaultAccessToken</span><span class="sxs-lookup"><span data-stu-id="329fe-159">-KeyVaultAccessToken</span></span>
<span data-ttu-id="329fe-160">Служба AccessToken для KeyVault</span><span class="sxs-lookup"><span data-stu-id="329fe-160">AccessToken for KeyVault Service</span></span>

```yaml
Type: String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="329fe-161">-ManagedServiceHostName</span><span class="sxs-lookup"><span data-stu-id="329fe-161">-ManagedServiceHostName</span></span>
<span data-ttu-id="329fe-162">Имя узла для логина управляемой службы</span><span class="sxs-lookup"><span data-stu-id="329fe-162">Host name for managed service login</span></span>

```yaml
Type: String
Parameter Sets: ManagedServiceLogin
Aliases: 

Required: False
Position: Named
Default value: localhost
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="329fe-163">-ManagedServicePort</span><span class="sxs-lookup"><span data-stu-id="329fe-163">-ManagedServicePort</span></span>
<span data-ttu-id="329fe-164">Номер порта для логина управляемой службы</span><span class="sxs-lookup"><span data-stu-id="329fe-164">Port number for managed service login</span></span>

```yaml
Type: Int32
Parameter Sets: ManagedServiceLogin
Aliases: 

Required: False
Position: Named
Default value: 50342
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="329fe-165">-Scope</span><span class="sxs-lookup"><span data-stu-id="329fe-165">-Scope</span></span>
<span data-ttu-id="329fe-166">Определяет область изменений контекста, например, применяются ли изменения только к текущему процессу или ко всем сеансам, запускаемым этим пользователем.</span><span class="sxs-lookup"><span data-stu-id="329fe-166">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

```yaml
Type: ContextModificationScope
Parameter Sets: (All)
Aliases: 
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="329fe-167">-ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="329fe-167">-ServicePrincipal</span></span>
<span data-ttu-id="329fe-168">Указывает, что учетная запись проходит проверку подлинности путем предоставления учетных данных субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="329fe-168">Indicates that this account authenticates by providing service principal credentials.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ServicePrincipalWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="329fe-169">-SkipValidation</span><span class="sxs-lookup"><span data-stu-id="329fe-169">-SkipValidation</span></span>
<span data-ttu-id="329fe-170">Пропуск проверки маркера доступа</span><span class="sxs-lookup"><span data-stu-id="329fe-170">Skip validation for access token</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AccessTokenWithSubscriptionId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="329fe-171">-Подписка</span><span class="sxs-lookup"><span data-stu-id="329fe-171">-Subscription</span></span>
<span data-ttu-id="329fe-172">Имя или идентификатор подписки</span><span class="sxs-lookup"><span data-stu-id="329fe-172">Subscription Name or ID</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SubscriptionName, SubscriptionId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="329fe-173">-TenantId</span><span class="sxs-lookup"><span data-stu-id="329fe-173">-TenantId</span></span>
<span data-ttu-id="329fe-174">Имя или идентификатор необязательного клиента</span><span class="sxs-lookup"><span data-stu-id="329fe-174">Optional tenant name or ID</span></span>

```yaml
Type: String
Parameter Sets: UserWithSubscriptionId, AccessTokenWithSubscriptionId, ManagedServiceLogin
Aliases: Domain

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ServicePrincipalWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionId
Aliases: Domain

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="329fe-175">-Confirm</span><span class="sxs-lookup"><span data-stu-id="329fe-175">-Confirm</span></span>
<span data-ttu-id="329fe-176">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="329fe-176">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="329fe-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="329fe-177">-WhatIf</span></span>
<span data-ttu-id="329fe-178">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="329fe-178">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="329fe-179">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="329fe-179">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="329fe-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="329fe-180">CommonParameters</span></span>
<span data-ttu-id="329fe-181">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="329fe-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="329fe-182">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="329fe-182">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="329fe-183">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="329fe-183">INPUTS</span></span>

### <span data-ttu-id="329fe-184">Подстрок</span><span class="sxs-lookup"><span data-stu-id="329fe-184">String</span></span>
<span data-ttu-id="329fe-185">Параметр "SubscriptionId" принимает значение типа String из конвейера.</span><span class="sxs-lookup"><span data-stu-id="329fe-185">Parameter 'SubscriptionId' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="329fe-186">Подстрок</span><span class="sxs-lookup"><span data-stu-id="329fe-186">String</span></span>
<span data-ttu-id="329fe-187">Параметр "SubscriptionName" принимает значение типа String из конвейера.</span><span class="sxs-lookup"><span data-stu-id="329fe-187">Parameter 'SubscriptionName' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="329fe-188">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="329fe-188">OUTPUTS</span></span>

### <span data-ttu-id="329fe-189">PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="329fe-189">PSAzureProfile</span></span>
<span data-ttu-id="329fe-190">Учетные данные, сведения о подписке, учетной записи и клиенте для пользователя, выполнившего вход.</span><span class="sxs-lookup"><span data-stu-id="329fe-190">Credentials, subscription, account, and tenant information for the logged in user.</span></span>

## <span data-ttu-id="329fe-191">Пуск</span><span class="sxs-lookup"><span data-stu-id="329fe-191">NOTES</span></span>

## <span data-ttu-id="329fe-192">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="329fe-192">RELATED LINKS</span></span>

